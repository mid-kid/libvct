project('libvct', 'c',
    meson_version: '>=1.2.0',
    version: '1.3.1'
)

cc = meson.get_compiler('c')

libvct = cc.find_library('vct', dirs : meson.current_source_dir() / 'prebuilt')
nitrosdk_dep = dependency('NitroSDK')

libvct_dep = declare_dependency(
    dependencies: [libvct, nitrosdk_dep],
    include_directories: include_directories('include')
)

meson.override_dependency('libvct', libvct_dep)
