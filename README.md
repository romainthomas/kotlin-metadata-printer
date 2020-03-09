Kotlin Metadata Printer
=======================

The Kotlin metadata printer is a free tool to print the Kotlin metadata in a human-readable format. The printer is
built on the ProGuard Core library and can process class files, zip files, jars or apks.

# Dependencies

As ProGuard works only with Java class files the tool uses the free dex2jar library to convert the dex files to
class files for processing, these are included in the libs/ folder. It requires a Java Runtime Environment (JRE 1.8 or higher).

# Building

You can build the Kotlin metadata printer jar by executing the following Gradle command:

    ./gradlew jar
    
Once built a jar will be created in build/libs/kotlin-metadata-printer.jar

# Executing

You can execute the printer directly through gradle as follows:

    ./gradlew run --args "input.{apk,jar,zip,class}"

Or you can execute the built printer jar as follows:

    java -jar build/libs/kotlin-metadata-printer.jar input.{apk,jar,zip,class}
    
# Options

    --filter=<classNameFilter> class name filter
    --output=<outputFile>      write output to this file instead of stdout
    --printclass               print corresponding class
    --printmetadata            print metadata
    --printmodule              print Kotlin module information

# License

The Kotlin metadata printer are distributed under the terms of the Apache License Version 2.0. Please consult the [license
page](LICENSE.md) for more details.

Copyright (c) 2002-2020 Guardsquare NV