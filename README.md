analytics-android-integration-kahuna
======================================

Kahuna integration for [analytics-android](https://github.com/Kahuna/segment-android-integration).

## Installation

To install the Kahuna-Segment integration, add this to your project gradle file:

```
allprojects {
  repositories {
    jcenter()
    maven { url "https://kahuna.github.io/kahuna-android/integration" }
    maven { url "https://kahuna.github.ios/kahuna-android/sdk" }
  }
}
```

Add this to your app level gradle file: 

```
compile ('com.kahuna.integration.android.segment:kahuna:+') {
  transitive = true
}
```

## Usage

After adding the dependency, you must register the integration with our SDK.  To do this, import the Kahuna integration:

```
import com.segment.analytics.android.integrations.kahuna.KahunaIntegration;
```

And add the following line:

```
Analytics analytics = new Analytics.Builder(this, "SEGMENT_KEY")
   .use(KahunaIntegration.FACTORY)
   .build();
```

Please see [our documentation](https://segment.com/docs/integrations/kahuna/) for more information.


## License

```
Copyright (c) 2016 Kahuna, Inc.
```
