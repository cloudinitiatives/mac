Change Prompt Color on you Mac


\[\033[COLOR_CODE_HERE\]PROMPT_ESCAPE_OR_TEXT_HERE\[\033[0m\]
Most Linux distributions use a little different format:

\e[COLOR_CODE PROMPT_ESCAPE\e[0m
The first portion before the desired prompt escape or text only begins painting the chosen color (e.g., \[\033[1;34m\]). To stop painting a color, you have to reset to another color or turn color off (e.g., \[\033[0m\]).

Here’s a comprehensive list of color encoding:

# Regular Colors
\[\033[0;30m\] # Black
\[\033[0;31m\] # Red
\[\033[0;32m\] # Green
\[\033[0;33m\] # Yellow
\[\033[0;34m\] # Blue
\[\033[0;35m\] # Purple
\[\033[0;36m\] # Cyan
\[\033[0;37m\] # White

# High Intensty
\[\033[0;90m\] # Black
\[\033[0;91m\] # Red
\[\033[0;92m\] # Green
\[\033[0;93m\] # Yellow
\[\033[0;94m\] # Blue
\[\033[0;95m\] # Purple
\[\033[0;96m\] # Cyan
\[\033[0;97m\] # White

# Background
\[\033[40m\] # Black
\[\033[41m\] # Red
\[\033[42m\] # Green
\[\033[43m\] # Yellow
\[\033[44m\] # Blue
\[\033[45m\] # Purple
\[\033[46m\] # Cyan
\[\033[47m\] # White

# High Intensty backgrounds
\[\033[0;100m\] # Black
\[\033[0;101m\] # Red
\[\033[0;102m\] # Green
\[\033[0;103m\] # Yellow
\[\033[0;104m\] # Blue
\[\033[10;95m\] # Purple
\[\033[0;106m\] # Cyan
\[\033[0;107m\] # White

#Replace any leading leading 0; with 1; for bold colors
#Replace any leading 0; with 4; to underline
Once you’ve decided on the appropriate prompt add export PS1=”<custom prompt>” to your .profile. For example, this is what the line in my .profile looks like:

export PS1="\[\033[1;34m\]\!\[\033[0m\] \[\033[1;35m\]\u\[\033[0m\]:\[\033[1;3