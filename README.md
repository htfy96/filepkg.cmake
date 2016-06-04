# filepkg.cmake

CMake library providing package query&install based on file pattern.

Currently it only supports `pacman`. `apt` support is on schedule.

![ScreenShot](https://github.com/htfy96/filepkg.cmake/raw/master/screenshot.gif)

## Quick start

### Put smartpkg.cmake under your module path

If you haven't set `CMAKE_MODULE_PATH`, the following line would set `{your_source_dir}/cmake/Modules` as an available module path where `filepkg.cmake` should be located.

```
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")
```

### Include and use

```
include(filepkg)
INSTALL_FILE(*/mysql/mysql.h)
```

if this step failed, `INSTALL_FILE_FAILED` would be set.

## Additional configuration

`INSTALL_FILE_NOCONFIRM` variable would skip confirmation before install

