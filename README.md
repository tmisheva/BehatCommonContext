Behat Common Contexts
=====================

Provide most common behat tests.

The only change from the original repository [novaway/BehatCommonContext](https://github.com/novaway/BehatCommonContext) is a fix for Select2 Version 3.

## Installation

The extension requires :

* Behat
* Mink extension

## Usage

Add dependencies with Composer :
``` bash
"require": {
    ...
    "tmisheva/common-contexts": "dev-master"
},
"repositories": [
    { "type": "vcs", "url": "git@github.com:tmisheva/BehatCommonContext.git" }
]
```

In `behat.yml`, enable desired contexts:

```yaml
default:
    suites:
        default:
            contexts:
                - nwcontext:form
                - nwcontext:formstone
                - nwcontext:select2

    # ...
    extensions:
        Novaway\CommonContexts\Extension: ~
```
or
```yaml
default:
  # ...
  suites:
    default:
      contexts:
        # ...
        - Novaway\CommonContexts\Context\Select2Context
```
