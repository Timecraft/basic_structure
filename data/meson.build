
# Install application icons.
icon_sizes = ['16','24','32','64','128','256']
foreach i : icon_sizes
  install_data (
  join_paths ('icons', meson.project_name () + '.' + i + '.svg'),
  install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i, 'apps')
  )
  install_data (
  join_paths ('icons', meson.project_name () + '.' + i + '.svg'),
  install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i + '@2', 'apps')
  )
endforeach


#Translate and install our .desktop file
i18n.merge_file(
    input: join_paths(meson.project_name() + '.desktop.in'),
    output: meson.project_name() + '.desktop',
    po_dir: join_paths(meson.source_root(), 'po'),
    type: 'desktop',
    install: true,
    install_dir: join_paths(get_option('datadir'), 'applications')
)


#Install .appdata.xml for AppCenter

i18n.merge_file(
    input: join_paths(meson.project_name() + '.appdata.xml.in'),
    output: meson.project_name() + '.appdata.xml',
    po_dir: join_paths(meson.source_root(), 'po'),
    install: true,
    install_dir: join_paths(get_option('datadir'), 'metainfo')
)
