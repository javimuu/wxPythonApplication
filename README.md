# wxPythonApplication

## Tutorials: http://zetcode.com/wxpython/

##Installing wxWidgets and wxPython On Ubuntu Or Debian

There are wxWidgets and wxPython packages in the standard software repositories for Debian and Ubuntu, but they are usually at least a few releases behind the current release, and in some cases many releases behind. Since many users prefer to use only packages installed from repositories (for easier package management) but still would like to have newest versions possible of their installed software, we have our own APT repository that is usually updated within a few days of each release. To use it to be able to keep your wx on the cutting edge release just follow these instructions.

    The packages and the repository meta-data are digitally signed, so you'll need to import the key into your apt's list of trusted keys in order to not get warnings about it.

        curl http://apt.wxwidgets.org/key.asc | sudo apt-key add - 

    Add the following lines to your /etc/apt/sources.list file (or use the "software sources" program under the "system" menu). Replace the "DIST" text with whatever is appropriate for your system. (See the table below for a list of supported distributions and architectures.)

        # wxWidgets/wxPython repository at apt.wxwidgets.org
        deb http://apt.wxwidgets.org/ DIST-wx main
        deb-src http://apt.wxwidgets.org/ DIST-wx main  

    For example, if your distro is Ubuntu Gutsy, then you would use the following configuration statements:

        # wxWidgets/wxPython repository at apt.wxwidgets.org
        deb http://apt.wxwidgets.org/ gutsy-wx main
        deb-src http://apt.wxwidgets.org/ gutsy-wx main  

    Run the this command to update your local copy of the package meta-data.

        sudo apt-get update  

    You can now use your favorite package selection tool to install or upgrade the wxWidgets and wxPython packages. Here's how to do it with apt-get:

        sudo apt-get install python-wxgtk2.8 python-wxtools wx2.8-i18n

    The packages libwxgtk2.8-dev and libgtk2.0-dev may need to be installed if a 3rd party application requires wxWidgets when building from source.

        sudo apt-get install python-wxgtk2.8 python-wxtools wx2.8-i18n libwxgtk2.8-dev libgtk2.0-dev

    These packages (and their dependencies) will replace earlier versions of wxPython and wxGTK in the same ReleaseSeries that may have been installed previously. There are a few other wx packages as well, but those listed above and their dependencies are the core that are needed for use with wxPython.
