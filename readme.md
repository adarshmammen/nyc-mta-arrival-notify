**Introduction**
------------

This a basic python script that reads the NYC MTA realtime feed API for subway data and outputs when the next arrival is for a given station. The output can be redirected as a text message using Twilio's API. 

This script uses the New York MTA real-time data feed for its subway system:

* [NYC MTA Live Feed Documentation](http://datamine.mta.info/sites/all/files/pdfs/GTFS-Realtime-NYC-Subway%20version%201%20dated%207%20Sep.pdf)
* [List of Live MTA Feeds](http://datamine.mta.info/list-of-feeds)
* [Register for an API key](http://datamine.mta.info/user/register)

Because the New York MTA real-time data feed uses the [GTFS-realtime](https://developers.google.com/transit/gtfs-realtime/) data exchange format (which is based upon [protocol buffers](https://developers.google.com/protocol-buffers/)) this script relies on kaporzhu's [protobuf3-to-dict](https://github.com/kaporzhu/protobuf-to-dict) package to convert the MTA's GTFS feed into a more python-friendly set of python dictionaries and lists.

**Requirements**
-------------------------------
This script relies on the following packages: Python language bindings for GTFS, protobuf3-to-dict, and dotenv to insert the API key provided by the MTA. If you use PIP, the following commands will do the trick:

    pip install --upgrade gtfs-realtime-bindings
    pip install protobuf3_to_dict
    pip install -U python-dotenv

Access to the MTA live feeds requires signing up for an API key from the NYC MTA: http://datamine.mta.info/user/register



The specific station ID is currently hardcoded in, and is set for the southbound Broadway-Lafayette stop. The list of subway stops and station IDs may be found in the MTA's collection of [*static* data feeds](http://web.mta.info/developers/developer-data-terms.html).

**License**
------------
Uses the MIT license.


