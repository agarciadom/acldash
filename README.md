ACL Dashboards
===

This Sparkl-based plugin provides a set of dashboards for quickly
checking what a role or a user can access on a Pentaho
installation. It is compatible with Pentaho 5.4 or later, as it
heavily depends on the PDI [Call
endpoint](http://wiki.pentaho.com/display/EAI/Call+Endpoint) step.

Most of this plugin can be used without any need for configuration,
but permission toggling requires additional setup because of a
[limitation](https://github.com/pentaho/pdi-platform-utils-plugin/issues/1)
in the "Call endpoint" step, which requires falling back to the old
[REST Client](http://wiki.pentaho.com/display/EAI/Rest+Client)
step. Please check the included `config.yaml` for details.

Basic usage
--

To use this plugin, go to the Pentaho User Console and access "Tools -> ACL Dashboards". The main dashboard will list the current usernames and passwords in the Pentaho installation. To access the details of a user or a role, simply click on it.

User dashboards list the roles of the selected user and indicate which files are visible to the user. The "visible" flag can be clicked to toggle the visibility of the resource to the user, as long as the visibility comes from the user itself and not one of its roles.

Role dashboards list the users with that role and indicate which files are visible to the role. The "visible" flag can be clicked to toggle its permissions as well.
