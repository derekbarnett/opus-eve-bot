opus-eve-bot
============

This is a quick and dirty hack of eve-bot to keep
it from blocking the use of opus on murmur servers.

The original eve-bot can be found here:
http://frymaster.127001.org/mumble/

Once eve-bot is providing an opus value, you would
be well served to use eve-bot rather than this hack.

See the original eve-readme.txt for detailed usage
instructions. The only thing which has changed here
is the new bot is named opus-eve-bot.py rather than
eve-bot.py, and opus-eve-bot provides opus values
on connection to the mumble server.

You need protobuf installed. After installation,
you can compile the python module with:

    protoc --python_out=. Mumble.proto

I use this bot as an audio test repeater, although
the original intent for eve-bot was slightly 
different. See eve-readme.txt for more information
regarding how you can use it. I run it with this
command:
    
    ./opus-eve-bot.py -r 'Audio Test' -e 'Audio Test' -d 10

This listens in a channel called Audio Test, and also
spawns the mimics to the same channel (no, the mimics
do not get their own mimics, so this does not cause
any problems.) When a person joins the Audio Test room,
a mimic is spawned for that individual and any audio
which the individual transmits is played back to them
on a 10 second delay. 

For whatever it's worth, I also create a subchannel in
Audio Test that is linked so that another person can
help troubleshoot without spawning their own mimic.

