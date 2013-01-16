require './lib/waveform'

task :default => :test

task :test do
  system "ruby test/*.rb"
end

namespace :gem do
	task :build do
		system 'gem build waveform.gemspec'
	end

	task :install do
		system "gem install --local waveform-#{Waveform::VERSION}.gem"
	end

	task :build_install => [:build, :install]
end

task :gem => 'gem:build_install'
