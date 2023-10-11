for macos

brew install qt5
brew install cmake


brew --prefix qt5   # you will got a path: /usr/local/opt/qt@5

edit ~/.bash_profile

export Qt5Widgets_DIR=/usr/local/opt/qt5/lib/cmake/Qt5Widgets
export Qt5Test_DIR=/usr/local/opt/qt5/lib/cmake/Qt5Test
export Qt5Core_DIR=/usr/local/opt/qt5/lib/cmake/Qt5Core
export Qt5_DIR=/usr/local/opt/qt5/lib/cmake
export Qt5Concurrent_DIR=/usr/local/opt/qt5/lib/cmake/Qt5Concurrent
export Qt5Gui_DIR=/usr/local/opt/qt5/lib/cmake/Qt5Gui

mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr/local ../
make
