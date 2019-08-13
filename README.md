# NodeBB LDAP authentication Plugin

This plugin was modified from https://github.com/smartameer/nodebb-plugin-office-ldap to allow for authentication using an OpenLDAP server.

The plugin allows a user to log in to NodeBB using credentials stored in an LDAP server. If the user doesn't currently exist in NodeBB, it will be created using the details retrieved from the LDAP server. Once installed, settings can be changed within the 'LDAP settings' menu in the 'Plugins' tab of the ACP

Please disable user registration in the NodeBB ACP (Settings>User>User Registraion>No Registration) when using this plugin.

Features of the plugin include:

* can login to NodeBB via email or an additional 'Filter' field (Plugins>LDAP settings>Filter) that is stored in the LDAP server.
* the email field MUST be set for each user in the LDAP server as the 'Filter' field is merely used to retrieve the email field
* on first login the username within NodeBB is generated from the 'User Name Field' chosen in the 'LDAP settings' menu and retrieved from the LDAP server (must be unique for each user).
* on first login the user 'Full Name' in NodeBB is generated using the 'Given Name' and 'Surname' fields  chosen in the 'LDAP settings' menu and retrieved from the LDAP server.

## Installation

    npm install nodebb-plugin-node-ldap

## Screenshots

### Desktop
![Desktop OfficeLDAP](screenshots/desktop.png?raw=true)
