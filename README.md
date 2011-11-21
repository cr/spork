# spork
### sparklines for your shell -- a Python implementation

Forked from <https://github.com/holman/spark> who did the original shell-script implementation.
For some inspiration on what to do with spork, I suggest you see his [Wiki](https://github.com/holman/spark/wiki).

I was dissatisfied with several aspects of holman's version, so here is another cr re-invention
of the wheel, and it improves on the following points:

 * Speed. We're talking about a factor of 10 or more.
 * Full support for floating point values (in Python format).
 * Deterministic behavior. No more value skipping, or weird bucketing behavior with small lists.
 * Argument handling. Who needs CSV? We want whitespace!
 * Pipe support by reading from cmdline.
 * Re-usability via Python class.

## Install

spork is a python script, so drop make sure it's executable (`chmod +x`), and it somewhere and make sure
the dirctory is added to your `$PATH`.

## Usage

Just run `spork` and pass it a whitespace-delimited list of numbers:

    spork 0 30 55 80 33 150
    ▁▂▃▄▂▇

Calling spork without arguments reads values from stdin. Invoke help with `spark -h`.

