This repo contains mozconfig files that I habitually use to build firefox.

Moving into github to save time manually copying these into every new device or VM.

You can read about mozconfig files here: https://firefox-source-docs.mozilla.org/setup/configuring_build_options.html

How to use this?
1. download the firefox source code
2. install this repo in your home dir: `git clone https://github.com/jaredhirsch/mozconfigs`
3. before building firefox, `export MOZCONFIG=~/mozconfigs/mozconfig` (for an artifact build)

Note that each mozconfig is configured to use a different output location (the "objdir" in mozilla jargon) where the build output is placed on disk (including partial caches of compiled output thanks to [sccache](https://github.com/mozilla/sccache) on supported platforms). This saves rebuild time if you regularly switch between different kinds of builds, but at the cost of additional disk space. Read about the different types of builds in the build options link above.

license: MPLv2 like the rest of firefox

author: jared hirsch
