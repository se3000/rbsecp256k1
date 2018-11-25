require 'bundler/gem_tasks'
require "rake/extensiontask"
require 'rubygems'

$LOAD_PATH.unshift('/Users/steve/workspace/rbsecp256k1/ext')

Rake::ExtensionTask.new "rbsecp256k1" do |ext|
  ext.lib_dir = "ext"
end

task :default do
  puts $LOAD_PATH
  priv_key = Secp256k1::PrivateKey.new(Secp256k1.generate_private_key_bytes)
  ctx = Secp256k1::Context.new
  Secp256k1::PublicKey.new(ctx, priv_key)
end
