# Librosa tutorial

In this tutorial, my goal is to get you set up to use librosa for audio and music analysis.
This tutorial will be interactive, and it will be best if you follow along on your own machine.
Feel free to bring along some of your own music to analyze!

We'll be using [Jupyter](http://jupyter.org/) notebooks and the [Anaconda](https://www.continuum.io/downloads)
Python environment with Python version 3.5.  It will be best if you follow the instructions below before
attending the tutorial, but installation disks will also be provided in case anything goes wrong or you require
assistance.

---

# Installing the dependencies

Before getting started with librosa, it's important to have a working environment with all dependencies
satisfied.  For this, we recommend using the [Anaconda](https://www.continuum.io/downloads) distribution of
Python 3.5.  (Older versions of Python are supported as well.)

Once your Anaconda environment is installed, you can install librosa through `conda-forge`:

```
conda install -c conda-forge librosa
```

## Audio codecs

Librosa requires a few additional packages to load audio data encoded in various formats (e.g., `mp3`, `ogg`,
`flac`, `m4a`).  The two main libraries used by librosa are [ffmpeg](https://ffmpeg.org/) and
[gstreamer](https://gstreamer.freedesktop.org/).  Both are optional, but you must install at least one
package.
Audio codec libraries are packaged differently on different platforms.

* On Linux, `ffmpeg` is available through `conda-forge` and is installed automatically when `librosa` is
installed through `conda-forge`.  GStreamer can be installed through your Linux distribution's package manager
(e.g., `apt-get install libgstreamer1.0-0` on Debian/Ubuntu).

* On OSX, `ffmpeg` is available through `conda-forge` and is installed automatically when `librosa` is
installed through `conda-forge`.  GStreamer can be installed by `brew install gstreamer` or by downloading
directly from the [gstreamer downloads](https://gstreamer.freedesktop.org/download/) page.

* On Windows, `ffmpeg` must be installed separately from the [ffmpeg downloads](http://ffmpeg.org/download.html) page.


For all operating systems, if you're using `gstreamer`, you will need to install `PyGObject` through `pip`:

```
pip install PyGObject
```

## Jupyter

The tutorial materials in this repository are provided in the form of [Jupyter](http://jupyter.org/)
notebooks.  Jupyter can be installed by the following command:
```
conda install jupyter
```
