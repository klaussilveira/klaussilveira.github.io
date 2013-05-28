require "fileutils"

bootstrap = [
  "_grid.scss",
  "_normalize.scss",
  "_reboot.scss",
  "_type.scss",
  "_variables.scss",
  "mixins/_clearfix.scss",
  "mixins/_breakpoints.scss",
  "mixins/_grid-framework.scss",
  "mixins/_grid.scss",
  "mixins/_hover.scss",
  "mixins/_lists.scss",
  "mixins/_visibility.scss",
  "utilities/_visibility.scss"
]

task :build do
  sh "bower install"

  bootstrap.each do |file|
    mkdir_p File.dirname("_sass/bootstrap/#{file}")
    cp "_bower/bootstrap/scss/#{file}", "_sass/bootstrap/#{file}"
  end

  sh "jekyll doctor"
  sh "jekyll build"
end

task default: %w[build]
