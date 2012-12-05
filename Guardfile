# added by cuke-pack

group :wip do
  guard 'cucumber', :env => :cucumber, :cli => '-p wip' do
    watch(%r{^features/.+.feature$})
    watch(%r{^(app|lib).*})          { 'features' }
    watch(%r{^features/support/.+$})          { 'features' }
    watch(%r{^features/step_definitions/(.+).rb$}) { 'features' }
  end
end

guard 'livereload' do
  watch(%r{app/views/.+\.(erb|haml|slim)$})
  watch(%r{app/helpers/.+\.rb})
  watch(%r{public/.+\.(css|js|html)})
  watch(%r{config/locales/.+\.yml})
  # Rails Assets Pipeline
  watch(%r{(app|vendor)(/assets/\w+/(.+\.(s[ac]ss|coffee|css|js|html))).*}) { |m| "/assets/#{m[3]}" }
end
