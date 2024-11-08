
To setup and build the entire project, run scripts/build.sh

mediamtx.yml is the configuration file.  the config is the default mediamtx.yml configuration, and at the very bottom is where we add our paths to expose.

Dockerfile.ffmpeg-hwa builds custom ffmpeg with hardware acceleration for rk3588.  It is robust and may have more items included than a developer desires.  The --enable options can be removed.  the dockerfile also includes SRT support for those wanting to test newer SRT protocol due to its robust security and real time video support.

Dockerfile.mediamtx-hwa build mediamtx server and copies in custom ffmpeg-hwa to ensure mediamtx server can utilize hardware acceleration.

docker-compose.yml brings the solution together.  Currently it is set to use as privileged for development use.  Device mappings can be included and are located commented out at the bottom.


More information can be found on mediatmtx at: https://github.com/bluenviron/mediamtx