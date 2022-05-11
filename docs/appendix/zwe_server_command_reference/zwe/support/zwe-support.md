# zwe support

[zwe](.././zwe) > [support](./zwe-support)

	zwe support [sub-command [sub-command]...] [parameter [parameter]...]

## Sub-commands

* [verify-fingerprints](./zwe-support-verify-fingerprints)

## Description

Collect and package Zowe runtime information for support purpose.

This command will collect these information:

- Environment
  * z/OS version
  * Java version
  * Node.js version
- Zowe configurations
  * Zowe manifest.json
  * Zowe configuration file
  * Zowe installation logs
  * Zowe PKCS#12 keystore if used
  * Zowe temporary configuration files under `<workspace>/.env`
  * Zowe APIML static registration files under `<workspace>/api-mediation/api-defs`
- Zowe runtime
  * Active running Zowe processes
  * Zowe job log
- Zowe fingerprints and validation result


## Parameters

Full name|Alias|Type|Required|Help message
|---|---|---|---|---
--target-dir||string|no||Target directory where the support package will be created.\nIf it is not specified, system temporary directory will be used.
### Inherited from parent command

Full name|Alias|Type|Required|Help message
|---|---|---|---|---
--help|-h|boolean|no||Display this help.
--debug,--verbose|-v|boolean|no||Enable verbose mode.
--trace|-vv|boolean|no||Enable trace level debug mode.
--silent|-s|boolean|no||Do not display messages to standard output.
--log-dir,--log|-l|string|no||Write logs to this directory.
--config|-c|string|no||Path to Zowe configuration zowe.yaml file.


## Errors

### Inherited from parent command

Error code|Exit code|Error message
|---|---|---
||100|If the user pass `--help` or `-h` parameter, the zwe command always exits with `100` code.
ZWEL0101E|101|ZWE_zowe_runtimeDirectory is not defined.
ZWEL0102E|102|Invalid parameter %s.
ZWEL0103E|103|Invalid type of parameter %s.
ZWEL0104E|104|Invalid command %s.
ZWEL0105E|105|The Zowe YAML config file is associated to Zowe runtime "%s", which is not same as where zwe command is located.
ZWEL0106E|106|%s parameter is required.
ZWEL0107E|107|No handler defined for command %s.
ZWEL0108E|108|Zowe YAML config file is required.
ZWEL0109E|109|The Zowe YAML config file specified does not exist.
ZWEL0110E|110|Doesn't have write permission on %s directory.
ZWEL0111E|111|Command aborts with error.
ZWEL0112E|112|Zowe runtime environment must be prepared first with "zwe internal start prepare" command.
ZWEL0120E|120|This command must run on a z/OS system.
ZWEL0121E|121|Cannot find node. Please define NODE_HOME environment variable.
ZWEL0122E|122|Cannot find java. Please define JAVA_HOME environment variable.
ZWEL0123E|123|This function is only available in Zowe Containerization deployment.
ZWEL0131E|131|Cannot find key %s defined in file %s.
ZWEL0132E|132|No manifest file found in component %s.
ZWEL0133E|133|Data set %s already exists.
ZWEL0134E|134|Failed to find SMS status of data set %s.
ZWEL0135E|135|Failed to find volume of data set %s.
ZWEL0136E|136|Failed to APF authorize data set %s.
ZWEL0137E|137|z/OSMF root certificate authority is not provided (or cannot be detected) with trusting z/OSMF option enabled.
ZWEL0138E|138|Failed to update key %s of file %s.
ZWEL0139E|139|Failed to create directory %s.
ZWEL0140E|140|Failed to translate Zowe configuration (%s).
ZWEL0142E|142|Failed to refresh APIML static registrations.
ZWEL0172E||Component %s has %s defined but the file is missing.