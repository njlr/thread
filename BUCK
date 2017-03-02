include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'boost-thread', 
  header_namespace = 'boost',
  exported_headers = subdir_glob([
    ('include/boost', '**/*.hpp'),
  ]),
  srcs = glob([
    'src/*.cpp',
  ]),
  platform_srcs = [
    ('^macos.*', glob(['src/pthread/**/*.cpp'])),
    ('^linux.*', glob(['src/pthread/**/*.cpp'])),
    ('^windows.*', glob(['src/win32/**/*.cpp'])),
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
