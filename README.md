# Issues:

## breakage during OS major version upgrade

After an OS major version upgrade (bookworm to trixie), during python package updates, I started seeing errors like this:

    Traceback (most recent call last):
      File "/usr/local/python-packages/transmission-rpc/bin/pip3", line 5, in <module>
        from pip._internal.cli.main import main
    ModuleNotFoundError: No module named 'pip'

I removed `/usr/local/python-packages/flexget/`, reapplied the `flexget` role, and that seemed to fix the problem.  I do not understand exactly what went wrong, but watch out for this during OS major version upgrades.
