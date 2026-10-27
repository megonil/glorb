project(
  'glorb',
  'cpp',
  default_options: ['cpp_std=c++23'],
)

lexer_lib = static_library('lexer', ['lexer.cpp'])
chunk_lib = static_library('chunk', ['chunk.cpp'])

compiler_lib = static_library('compiler', ['compiler.cpp'], link_with: [lexer_lib, chunk_lib])

vm_lib = static_library('vm', ['vm.cpp'], link_with: [chunk_lib])

executable('glorb', 'main.cpp', link_with: [vm_lib, compiler_lib])
