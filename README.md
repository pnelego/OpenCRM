# OpenCRM
The first ever truely free and open source cloud CRM software.


# Modules
Modules for this software can be written in a multitude of languages, as long as it can be referenced directly.

# Server Modules
A server module will extend the default API functionality by loading off the script in your modules folder.
This script can be called anything with some extra server config, but by default OpenCRM will parse for a script
called "launch.conf".

the launch.conf file is set in JSON and must be formated accordingly. The following Keys are required in the
head object:

{
    "title": "Module title",
    "version: "Module version",
    "launch": "<launch command>"
    "keys": [
        {
            "path":"<path string from root>",

        }
    ]
} 

In order to get the script to load your parsed command, the script must accept the following arguments:

"--port '<the port provided from openCRM>' "


All server modules run on internal localhost and function as their own servers. OpenCRM will then redirect choice requests to that
port and encrypts them with a key shared by both OpenCRM and the worker function server.



# How to submit changes
I will openly use Github for these requests (using pull requests). You may also send patches in the relevant mailing lists.
(mailing list email will become avalible soon.)

All changes to mainline will be extensivly reviewed. 