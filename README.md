Read-only mirror of the Forgejo releases and git repository. The [instructions to get Forgejo](https://forgejo.org/download/) work exactly the same when replacing **codeberg.org** with **code.forgejo.org**.

* secrets.CODE_FORGEJO_TOKEN
  code.forgejo.org/forgejo-mirror user - token CODE_FORGEJO_TOKEN https://code.forgejo.org/forgejo/forgejo - write:package, write:repository, read:user
* vars.DOER
  Forgejo user that provided secrets.CODE_FORGEJO_TOKEN - e.g. forgejo-mirror
* vars.DESTINATION
  Forgejo instance of the mirror - e.g. code.forgejo.org
* vars.OWNER
  Forgejo owner of the mirror - e.g. forgejo
* secrets.TEST_FORGEJO_TOKEN
  code.forgejo.org/forgejo-mirror user - token CODE_FORGEJO_TOKEN https://code.forgejo.org/forgejo/forgejo - write:package, write:repository, read:user
* vars.TEST_DOER
  if TEST is true,  Forgejo user that provided secrets.TEST_FORGEJO_TOKEN - e.g. forgejo-mirror
* vars.TEST_DESTINATION
  if TEST is true, Forgejo instance where the images are pushed - e.g. v9.next.forgejo.org
* vars.TEST_OWNER
  if TEST is true,  Forgejo owner to which the images are pushed - e.g. forgejo
* vars.TEST
  if false secrets.CODE_FORGEJO_TOKEN is used to push images to vars.DESTINATION/vars.OWNER
  if true secrets.TEST_FORGEJO_TOKEN is used to push images to vars.TEST_DESTINATION/vars.TEST_OWNER
* vars.TEST_VERSION
  if set force a mirror of this version regardless - e.g. 7.0.5
* vars.VERBOSE
  `set -x` or `# set -x`
