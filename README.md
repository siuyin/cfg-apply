# cfg-apply templated configuration tool

## Examples

local.cfg.yaml:

    ---
    cfg:
      passwd: "MyP@sSW0rd"

deploy.template:

    export PASSWD={{.cfg.passwd}}

example run:

    cfg-apply local.cfg.yaml deploy.template > deploy.secrets
    . deploy.secrets # PASSWD environment var now set
