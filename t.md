# TASKS Aliases
  alias t='python ~/lib/t/t.py --task-dir ~/tasks --list tasks'
  alias w='python ~/lib/t/t.py --task-dir ~/tasks --list work'
  alias b='python ~/lib/t/t.py --task-dir . --list bugs'

### Add a Task
't [task description]'
t Clean the apartment.

### List Your Tasks
't'
t

### Finish a Task
't -f ID'
t -f 31

### Edit a Task
't -e ID [new description]'
t -e 30 Clean the entire apartment.

## Sed-style substitution strings:
't -e ID /bad/good/'
t -e 9 /more/a lot more/

### Delete the Task List if it's Empty
alias t='python ~/path/to/t.py --task-dir ~/Desktop --list todo.txt --delete-if-empty'

### Count Your Tasks
't | wc -l'

### Put Your Task Count in Your Bash Prompt
export PS1='[$(t | wc -l | sed -e"s/ *//")]'" $PS1"

### Multiple Lists
alias g='python ~/path/to/t.py --task-dir ~/tasks --list groceries'
alias m='python ~/path/to/t.py --task-dir ~/tasks --list music-to-buy'
alias w='python ~/path/to/t.py --task-dir ~/tasks --list wines-to-try'

### Distributed Bugtracking
alias b='python ~/path/to/t.py --task-dir . --list bugs'

