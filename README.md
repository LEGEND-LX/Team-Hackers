# Team-Hackers
https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/cli.gif


https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/socialanalyzerlogo_.png


Social-Analyzer - API, CLI & Web App for analyzing & finding a person's profile across social media websites. It includes different string analysis and detection modules, you can choose which combination of modules to use during the investigation process.

The detection modules utilize a rating mechanism based on different detection techniques, which produces a rate value that starts from 0 to 100 (No-Maybe-Yes). This module intended to have less false positive, and it's documented in this Wiki link

The analysis and public extracted information from this OSINT tool could help in investigating profiles related to suspicious or malicious activities such as cyberbullying, cybergrooming, cyberstalking, and spreading misinformation.

This project is "currently used by some law enforcement agencies in countries where resources are limited".

Social Analyzer is in a league of its own and is a very impressive tool that I thoroughly recommend for Digital Investigators and OSINT practitioners - by Joseph Jones, Founder of Strategy Nord, Unita Insight and OS2INT.

So·cial Me·di·a
Websites and applications that enable users to create and share content or to participate in social networking - Oxford Dictionary

Security Testing
-------------------------------------              ---------------------------------
|        Security Testing           |              |        Social-Analyzer        |
-------------------------------------              ---------------------------------
|   Passive Information Gathering   |     <-->     |   Find Social Media Profiles  |
|                                   |              |                               |
|    Active Information Gathering   |     <-->     |    Post Analysis Activities   |
-------------------------------------              ---------------------------------
Find Profile CLI (Fast)
https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/cli.gif

https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/cli.gif

Features
String & name analysis (Permutations and Combinations)
Find profile using multiple techniques (HTTPS library & Webdriver)
Multi layers detections (OCR, normal, advanced & special)
Visualized profile information using Ixora (Metadata & Patterns)
Metadata & Patterns extraction (Added from Qeeqbox osint project)
Force-directed Graph for Metadata (Needs ExtractPatterns)
Search by top ranking, or by country (Alexa Ranking)
Profiles stats and static info (Category country)
Auto-flirtation to unnecessary output
Search engine lookup (Google API - optional)
Custom search queries (Google API & DuckDuckGo API - optional)
Profile screenshot, title, info and website description
Find name origins, name similarity & common words by language
Custom user-agent, proxy, timeout & implicit wait
Python CLI & NodeJS CLI (limited to FindUserProfilesFast option)
Grid option for faster checking (limited to docker-compose)
Dump logs to folder or terminal (prettified)
Adjust findinggetting profile workers (default 15)
Re-checking option for failed profiles
Filter profiles by good, maybe, and bad
Save the analysis as JSON file
Simplified web interface and CLI
Running Example (Simple)
pip3 install social-analyzer
python3 -m social-analyzer --username "johndoe" --metadata --top 100
Running Example (Custom)
#install social-analyzer
pip3 install social-analyzer

#specific websites
python3 -m social-analyzer --username "johndoe" --websites "youtube pinterest tumblr"

#specific websites with metadata and extraction
python3 -m social-analyzer --username "johndoe" --websites "youtube pinterest tumblr" --metadata --extract --trim

#all websites with metadata, extraction, filter all profiles with all status
python3 -m social-analyzer --username "johndoe" --websites "all" --metadata --extract --trim --filter "all" --profile "all"
Running Example (as object)
from importlib import import_module
SocialAnalyzer = import_module("social-analyzer").SocialAnalyzer(silent=True)
results = SocialAnalyzer.run_as_object(username="johndoe",silent=True)
print(results)
Running Example (as object with specific websites, metadata and extraction)
from importlib import import_module
SocialAnalyzer = import_module("social-analyzer").SocialAnalyzer(silent=True)
results = SocialAnalyzer.run_as_object(username="johndoe", websites="youtube pinterest tumblr", metadata=True, extract=True, silent=True)
print(results)
Help (python3 -m social-analyzer --h)
Required Arguments:
  --username   E.g. johndoe, john_doe or johndoe9999

Optional Arguments:
  --websites    A website or websites separated by space E.g. youtube, tiktokor tumblr
  --mode        Analysis mode E.g.fast -> FindUserProfilesFast, slow -> FindUserProfilesSlow or special -> FindUserProfilesSpecial
  --output      Show the output in the following format: json -> json outputfor integration or pretty -> prettify the output
  --options     Show the following when a profile is found: link, rate, titleor text
  --method      find -> show detected profiles, get -> show all profiles regardless detected or not, all -> combine find & get
  --filter      Filter detected profiles by good, maybe or bad, you can do combine them with comma (good,bad) or use all
  --profiles    Filter profiles by detected, unknown or failed, you can do combine them with comma (detected,failed) or use all
  --countries   select websites by country or countries separated by space as: us br ru
  --top         select top websites as 10, 50 etc...[--websites is not needed]
  --extract     Extract profiles, urls & patterns if possible
  --metadata    Extract metadata if possible (pypi QeeqBox OSINT)
  --trim        Trim long strings
  --gui         Reserved for a gui (Not implemented)
  --cli         Reserved for a cli (Not needed)

Listing websites & detections:
  --list        List all available websites

Setting:
  --headers     Headers as dict
  --logs_dir    Change logs directory
  --timeout     Change timeout between each request
  --silent      Disable output to screen
Open in Cloud Shell
https://img.shields.io/static/v1?label=%3E_&message=Open%20in%20Cloud%20Shell&color=3267d6&style=flat-square
Special Detections
Facebook (Phone number, name or profile name)
Gmail (example@gmail.com)
Google (example@example.com)
Running Issues
Remember that existing profiles show status:good or rate:%100
Some websites return blocked or invalid <- this is the intended behavior
Use Proxy, VPN, TOR or anything similar for periodic suspicious-profiles checking
Do not mix FindUserProfilesFast, with FindUserProfilesSlow and ShowUserProfilesSlow
Change the user-agent to most updated one or increase the random time between requests
Use the slow mode (Not available in the CLIs) to avoid running into blockingresults issue
Resources
DuckDuckGo API, Google API, NodeJS, bootstrap, selectize, jQuery, Wikipedia, font-awesome, selenium-webdriver & tesseract.js
Let me know if I missed a reference or resource!
DisclaimerNotes
Make sure to download this tool from GitHub
This is a security project (Treat it as a security project)
If you want your website to be excluded from this project list, please reach out to me
This tool meant to be used locally not as a service (It does not have any type of Access Control)
For issues related to modules that end with -private or under the private group, reach out directly to me (do not open an issue on GitHub)
Interviews
Console 37
Some NewsArticles
5 Open-Source Intelligence (OSINT) GitHub Repositories For Every Security Analyst (Cyber Security)
You can use social-analyzer in the BlackArch penetration testing distribution by installing blackarch-social
Articles
kitploit professionalhackers secnhack meethackers raidforums redpacketsecurity hacking reviews hacking land securityonline skynettools luca-mercatanti pentesttools anonymousmedia ddosi tenochtitlan-sec modernnetsec haktechs haxf4rall hacker-gadgets mrhacker sector035 hackernews

Other projects
https://raw.githubusercontent.com/qeeqbox/.github/main/data//chameleon.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//honeypots.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//analyzer.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//osint.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//url-sandbox.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//mitre-visualizer.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//woodpecker.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//docker-images.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//seahorse.png https://raw.githubusercontent.com/qeeqbox/.github/main/data//rhino.png
