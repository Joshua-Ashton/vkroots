project('vkroots', 'cpp', meson_version: '>=0.58.0', default_options: [
  'cpp_std=c++20',
  'warning_level=2',
])

vkroots_dep = declare_dependency(
  include_directories : include_directories('.'),
  version             : meson.project_version(),
)

meson.override_dependency('vkroots', vkroots_dep)

install_headers('vkroots.h')

pkgconfig = import('pkgconfig')
pkgconfig.generate(
  version: meson.project_version(),
  filebase: meson.project_name(),
  name: meson.project_name(),
  description: 'Vulkan layers library',
  subdirs: '.'
)
