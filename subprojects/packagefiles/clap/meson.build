project(
    'clap',
    'rust',
    default_options: ['rust_std=2021'],
    license: 'MIT OR Apache-2.0',
    version: '4.5.20',
)

lib = static_library(
    'clap',
    dependencies: [dependency('clap_builder', version: ['= 4.5.20'])],
    native: true,
    rust_args: [
        '--cfg=feature="error-context"',
        '--cfg=feature="help"',
        '--cfg=feature="std"',
        '--cfg=feature="usage"',
    ],
    sources: files('src/lib.rs'),
)

dep = declare_dependency(link_with: lib)
meson.override_dependency('clap', dep)
