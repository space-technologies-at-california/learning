# STAC Learning Algorithms

## Setting up "Learning"

Note: these install instructions are based on the installation
structions for OpenAI's spinningup found here:
`https://spinningup.openai.com/en/latest/user/installation.html`.

Also note that I've only tested this on Mac.  I suspect it will
work with Linux, but am less sure about Windows.  (Mostly because
OpenAI says they're not sure whether it works with Windows!)

1. First, we will create a virtual environment for learning:
``virtualenv -p `which python3` stac``

2. Then, activate this environment:
`source stac/bin/activate`

Always activate this environment before using this repo.
You can exit the environment by typing `deactivate` when you're done working.

3. Install OpenMPI [This section is OS-dependent]:

- Ubuntu: `sudo apt-get update && sudo apt-get install libopenmpi-dev`
- Mac: `brew install openmpi`

4. If you haven't already cloned this git repo, clone it
and navigate into it:
```
  git clone https://github.com/space-technologies-at-california/learning
  cd learning
```

5. Use pip to install dependencies:
`pip install -e .`

Note that you must be in the `learning` directory to do this.

6. Check that installation was successful.
From within the learning directory, run `python test.py`.
This should begin training an agent for a `LunarLander`
environment.

This will run for a while; once it's done, you can run
`python -m spinup.run plot data/test1`
to see a plot of the results of this training.

You can also run
`python -m spinup.run test_policy data/test1
to see a video of the trained policy.
