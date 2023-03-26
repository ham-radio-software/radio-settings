# Radio Settings for D-Rats

Known Radio settings for D-Rats use.

This is a YAML file that is planned to bge used to assist
in adding Radios to D-Rats, primarily for setting the serial
baud rate.

This file is maintained in [YAML](https://yaml.org/spec/) format.

Each entry has the following entries:

* Name, the radio model
* Baud Rate for the radio

Optional information is if the radio port supports
additional signaling such as DSR/DTR.
Since most do not, that can omitted from the definition.
The dsr is just in the example below to show how it would be set in case
we get a radio that provides the very useful DSR signal.

Advanced maintainers can copy the tests/pre-commit script to inside the
.git/hooks directory which if the proper tools are installed, will test
the format of the files in a git commit action.  This requires shellcheck,
yamllint, and codespell to be installed.

```yaml
---
radios:
 - name: Radio_name
   baud: 9600
   dsr: false
```
