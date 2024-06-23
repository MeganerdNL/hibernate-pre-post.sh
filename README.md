# hibernate-pre-post.sh
You should place this script in:
- '/usr/lib/systemd/system-sleep' (systemd)
- '/etc/elogind/system-sleep' (non-systemd)
and make it executable.
See 'man 1 loginctl', section 'Hook directories' for more information.

Some devices do not function after hibernate, this script can solve that problem.
It disables kernel module(s) pre-hibernate and enables kernel module(s) post-hibernate.
You can add "hybrid-sleep" in the script too, if you use that.
