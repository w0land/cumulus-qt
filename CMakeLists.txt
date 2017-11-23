find_package(Qt5Quick REQUIRED)
find_package(Qt5Core REQUIRED)
find_package(Qt5Sql REQUIRED)
find_package(Qt5Gui REQUIRED)
find_package(Qt5Widgets REQUIRED)
find_package(Qt5QuickWidgets REQUIRED)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)

set(srcs
    CppFiles/Util.cpp
    CppFiles/DbConnection.cpp
    CppFiles/DataController.cpp
    CppFiles/YWeatherController.cpp
    CppFiles/Forecast.cpp
    CppFiles/SettingsController.cpp
    CppFiles/SearchLocation.cpp
    CppFiles/OwmWeatherController.cpp
    CppFiles/ThreadWorker.cpp
    CppFiles/WeatherType.cpp
    CppFiles/AbstractWeatherController.cpp
    CppFiles/TrayController.cpp
    CppFiles/CreditsAuthor.cpp
    CppFiles/CustomImageProvider.cpp
    CppFiles/FontImageProvider.cpp
    CppFiles/WundWeatherController.cpp
    CppFiles/MainWindow.cpp
    main.cpp
)

qt5_add_resources(resource_files qml.qrc)
add_executable(cumulus-qt ${srcs} ${resource_files})
target_link_libraries(cumulus-qt Qt5::Core Qt5::Quick Qt5::Sql Qt5::Gui Qt5::Widgets Qt5::QuickWidgets)
