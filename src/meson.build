jedit_sources = [
  'main.vala',
  'window.vala',
]

jedit_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

jedit_sources += gnome.compile_resources('jedit-resources',
  'jedit.gresource.xml',
  c_name: 'jedit'
)

executable('jedit', jedit_sources,
  vala_args: '--target-glib=2.50',  dependencies: jedit_deps,
  install: true,
)
