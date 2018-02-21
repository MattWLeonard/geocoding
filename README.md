# geocoding
The first (and only so far) script here accesses a geocoding API (in this case Google) which returns a response in JSON format for each address. The input can be either a text file with one address per line, which will then be converted into a python list (this is commented out), or a python list of addresses typed or pasted into this script. The outputs are 1) a python list of reformatted addresses with latitude and longitude coordinates as well as precision of the geocode match, and 2) the same information printed to the python interpreter.

A large portion of this script was taken from an in-class demonstration by Professor William Drummond at Georgia Institute of Technology, but I have modified it to include both possible methods for inputting addresses, and to address a problem I encountered when executing test runs. The problem is: some addresses at random will return a status "OVER_QUERY_LIMIT" which causes the script to throw an error. I have used if/else statements to tell the script to output NULL instead of the normal outputs when this problem is encountered, and then move on to the next address. I'm not actually over Google's query limit, as I am still able to geocode more addresses after the error is encountered, so I don't know why this error seems to happen at random.

I should probably note that Google documentation states that results from its geocoding API can only be displayed on a Google Map. This script is provided for demonstration purposes only.
