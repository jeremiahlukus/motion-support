#!/usr/bin/env rake
$:.unshift("/Library/RubyMotion/lib")
require 'motion/project/template/ios'
require "bundler/gem_tasks"
Bundler.setup
Bundler.require

require 'motion-support'

Motion::Project::App.setup do |app|
  # Use `rake config' to see complete project settings.
  app.name = 'MotionSupport'
  app.detect_dependencies = false

  app.sdk_version = '10.3'
  app.deployment_target = '9.0'

  files = [
    '/Users/naiyyarabbas/Downloads/motion-support/motion/_stdlib/date.rb',
    '/Users/naiyyarabbas/Downloads/motion-support/motion/_stdlib/array.rb',
    '/Users/naiyyarabbas/Downloads/motion-support/motion/_stdlib/cgi.rb',
    '/Users/naiyyarabbas/Downloads/motion-support/motion/_stdlib/time.rb',
    '/Users/naiyyarabbas/Downloads/motion-support/motion/_stdlib/enumerable.rb'
  ]

  files.each do |f|
    app.ordered_build_files.delete(f)
  end

  files.each do |f|
    app.ordered_build_files.unshift(f)
  end
end
