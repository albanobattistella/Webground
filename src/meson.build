install_subdir('.', install_dir : pkgdatadir, exclude_files: ['re.sonny.Webground', 'meson.build'])

bin_conf = configuration_data()
bin_conf.set('GJS', find_program('gjs').path())
bin_conf.set('PACKAGE_VERSION', meson.project_version())
bin_conf.set('PACKAGE_NAME', meson.project_name())
bin_conf.set('prefix', prefix)
bin_conf.set('libdir', join_paths(get_option('prefix'), get_option('libdir')))
bin_conf.set('datadir', datadir)
bin_conf.set('pkgdatadir', pkgdatadir)

configure_file(
  input: 're.sonny.Webground',
  output: 're.sonny.Webground',
  configuration: bin_conf,
  install: true,
  install_dir: get_option('bindir')
)

