

<p align="center">
  <a href="https://central.sonatype.com/artifact/io.github.lilytreasure/multiplatformContacts"><img alt="Profile" src="https://badgen.net/badge/Maven Central/v1.0.1/blue?icon=github"/></a>
</p><br>

<p align="center">
👻 Multiplatform Contacts is a straight forward library used to get  Contacts in Android and iOS.
</p><br>







### sample iOS
<p align="center">
<img src="https://github.com/Lilytreasure/MultiplatformContacts/assets/78819932/39de24b2-0ffd-4192-bb18-6c4b3ee12121" width="268"/>
</p>



### On Android

Add the following on your Manifest file:
```xml
  <uses-permission android:name="android.permission.READ_CONTACTS" />
```

### Gradle

You can add a dependency inside the `androidMain` or `commonMain` source set:
```gradle
commonMain.dependencies {
    implementation("io.github.lilytreasure:multiplatformContacts:1.0.1")
}
```
## Usage


```kotlin
    var phoneNumber by remember { mutableStateOf("") }
    val multiplatformContactsPicker = pickMultiplatformContacts(onResult = {number->
        phoneNumber = number
    })

  Column(Modifier.fillMaxWidth(), horizontalAlignment = Alignment.CenterHorizontally) {
            Button(onClick = {
                multiplatformContactsPicker.launch()
            }) {
                Text("Load contacts")
            }
            Text(text = phoneNumber)
        }

```
