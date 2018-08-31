sbt_dist(
  name='coursier-cli-dist',
  sources=rglobs('*.scala', '*.sbt'),
)

jar_library(
  name='coursier-snapshot'
  jars=[
    scala_jar(org='io.get-coursier', name='coursier', rev='1.1.0-SNAPSHOT'),
  ],
  dependencies=[
    ':coursier-cli-dist',
  ],
)

jvm_binary(
  name='coursier-cli',
  basename='coursier-cli',
  dependencies=[
    ':coursier-snapshot',
  ],
  main='coursier.cli.Coursier',
)
