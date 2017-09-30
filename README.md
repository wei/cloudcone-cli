# cloudcone-cli
Cloudcone commandline tool. Wrapper for https://api.cloudcone.com.

## Installation
```
$ curl -sSLO https://prod.download/cloudcone-cli
$ chmod +x cloudcone-cli
```

## Usage
First set `CC_KEY` and `CC_HASH` environment variables, or run `CC_KEY=[...] CC_HASH=[...] cloudcone-cli [...]`.

```text
Usage:
    cloudcone-cli [action] [id] [option ...]

Available actions:
    boot
    graphs
    info
    reboot
    shutdown
    status

Actions available for compute instances only:
    list
    list-os
    create              --payload
    reinstall-os        --payload
    reset-password      --payload
    resize              --payload

Options:
    -C, --compute       Compute instance (Default)
    -D, --dedicated     Dedicated instance
    -d, --payload       Payload to send with request
    -h, --help          Display this usage message and exit
    -v, --version       Prints version and exit
```
Omit `--payload` for an interactive form.

For prettier json outputs, pipe it to `| python -m json.tool` or other json beautify programs.

## Author
Wei He *github@weispot.com*

## License
[MIT](LICENSE)
