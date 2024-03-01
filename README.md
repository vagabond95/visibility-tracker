VisibilityTracker for Jetpack Compose [![](https://jitpack.io/v/hevinxx/visibility-tracker.svg)](https://jitpack.io/#hevinxx/visibility-tracker)
=====================================

VisibilityTracker is designed for Jetpack Compose that enables developers to easily monitor and respond to changes in the visibility of composables within the user interface. Whether you're building dynamic UIs that react to user scrolling or need to trigger actions based on the visibility of elements, VisibilityTracker provides a simple yet powerful solution.

Features
--------

*   **Visibility Detection**: Automatically detects when a composable's visibility changes, based on a specified visibility threshold.
*   **Flexible Callbacks**: Execute custom actions with the `onVisibleRatioChanged` callback, which provides the visible ratio of the composable as a float value.
*   **Easy Integration**: Seamlessly integrates with your Jetpack Compose UI with minimal setup.

How It Works
------------

VisibilityTracker leverages Jetpack Compose's `onGloballyPositioned` to monitor composables' positions and calculate their visibility ratio. When the visibility ratio crosses a predefined threshold, the `onVisibleRatioChanged` callback is triggered, allowing for custom actions based on the visibility state of the composable.

Usage
-----

To use VisibilityTracker, wrap your composable with the `VisibilityTracker` function and provide a lambda for the `onVisibleRatioChanged` callback:

```kotlin
VisibilityTracker(
    onVisibleRatioChanged = { visibilityRatio ->
        // Perform actions based on the visibility ratio
    }
) {
    // Your composable content here
}
```

Installation
------------

Step1. Add it in your root build.gradle at the end of repositories:
```gradle
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```
or in your settings.gradle.kts if you're using kotlin DSL:
```kts
dependencyResolutionManagement { 
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories { 
        mavenCentral()
        maven { url = uri("https://jitpack.io") } 
    }
}
```

Step2. Add the dependency:
```gradle
dependencies {
    implementation 'com.github.hevinxx:visibility-tracker:Tag'
}
```
Contributing
------------

We welcome contributions to VisibilityTracker! If you have suggestions for improvements or bug fixes, please feel free to open an issue or submit a pull request.

License
-------

VisibilityTracker is open-source software licensed under the MIT license.
