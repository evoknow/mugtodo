## README
I was finally fedup with all the TODO apps that I have tried. I had been trying and buying many TODO apps
over the years. I would find a shiney new one and try it for a few days/weeks/months and get bored and
never try it again. I finally realized why. I am a developer. I cannot be satified with the other
guy's TODO app. So I had to write my own the way I would want it to be.  So here it is:

A command-line TODO app that does what I want. If you like it, good luck! Maybe you will
like it for a short while and get bored with it! :)

The biggest advantages that I wanted to have in my iteration of the command-line TODO app:
* Create lists for me, others (like my children, spouse, or staff members)
* Export the list as .txt, .pdf, .html, .json etc. to make it easy to print or share
* Text the list to someone
* Generate interesting reports about time spent, due/past-due/late and accomplishments

=== GENERAL OPTIONS:
* --list <name> --for <name> .................... sets the namned person as the owner of a list. Defaults to: $USER
* --add <item> --list <name> .................... adds the item to the named list
* --add <item> --list <name> --tag <tag name> ... adds the item to the named list with given tag
* --add <item> --list <name> --for <name> ....... assigns the item to the named owner 
* --add <item> --list <name> --due <datetime> ... adds the item in the named list with a due date/time
* --change #n something -list <name>............. changes nth item in the named list
* --delete #n --list <name> ..................... delete nth item from the named list;
* --delete --list <name>......................... deletes the named list
* --list all .................................... shows all lists and their items
* --list <name> ................................. shows specified list items

=== STATUS MANAGEMENT:
--done #n --list <name>.......................... marks #nth item as done in list
--start #n --list <name>......................... starts the #nth item in the list 
--stop  #n --list <name>......................... stops the #nth item in the list
--due #n <date time> --list <name> .............. assigns a due date/time for #nth item in the named list (remembers due date history)
--time #n <day:hour:min> --list <name>........... adds days, hours, minutes to the #nth item in the named list (time reporting)
--note #n <text> --list <name> .................. adds a note to the nth item in the named list

=== SEARCH / REPORT / EXPORT OPTIONS
* --stats ....................................... shows various stats
* --find <keyword> .............................. searches items in all lists
* --find <keyword> --for <name> ................. searches items for all lists for named person
* --report <short-name> --for <name>............. shows named report for named person
* --export --file <name> --list <name> .......... exports the named list to a file. Supports: .md (markdown), .pdf, .html, .json, .txt
* --email <addr> --list <name> .................. sends the list via email to named address
* --text <addr/number> --list <name> ............ sends the list via imessage to named icloud email/phone

=== REPORTS
* due-(today|tomorrow|this-week|last-week|next-week|this-month|next-month|mon-yyyy|yyyy) 
* past-due
* past-due-by-(1...n)-days
* poorly-plannned
* need-tlc
* accomplishments

=== ADVANCED OPTIONS:
* --read <filename> --list <name> ................ reads the given .txt, .json file and adds or updates the items in the named list
* --set <option> ................................. sets configuration option

=== CONFIGURATION OPTIONS
--set my-name <name> ....... sets the name of default owner from $USER to <name>
--set my-email <email> ..... sets the email address of the default owner
--set person <name> <email> <imessage address/number> ... creates a --for target
--set password 


=== FUTURE OPTIONS
* --encrypt --list <name> ... makes a list encrypted 
