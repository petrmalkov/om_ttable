# om_ttable - Online Meditations time table (SY)

It takes some static time-sites and adds from youtube channels upcoming videos and premieres for the next (or current) day.  
Youtube video titles will be saved in origin language and added one more translated by google cli translator.

Get it to find more details (script does it automatically).  
    
    git clone https://github.com/soimort/translate-shell.git  
    cd translate-shell/  
    ./translate -T  # shows supported languages  
    ru - russian  
    uk - ukranian  
    en - english  
    it - italian  
    ... 

# DO THIS:  

    git clone https://github.com/petrmalkov/om_ttable.git  
    cd om_ttable/  

*.days - days of week translated to specific language.  
*.static - files with static time table for days (1-monday till 7-sunday), translated to specific language.  
format of lines:  
    
    time~link~title~country or channel  
    
any more fields with ~ separator (must to be for new line in output)  

add these files for your language  

# HOWTO RUN:  

    ./script language path_to_output_file flag  

By default script gets videos for the next day.  
But if you missed that moment and you want to get for the current day, print any word on place of flag.  
Output file will be sorted by time mixing static and dynamic data.  

# Examples:  

For russian and next day  

    ./script ru /tmp/out  

For ukranian and current day  

    ./script uk /tmp/out today  

