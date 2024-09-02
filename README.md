# ZoomLiveLiness

## Documentation

### Download the release Framework file

### Then Extract the file and add the framework to your project by dragging and dropping the framework to your project.

### Add the following permissions in your info.plist file

```
<key>NSCameraUsageDescription</key>
<string>$(PRODUCT_NAME) camera use</string>
<key>NSMicrophoneUsageDescription</key>
<string>$(PRODUCT_NAME) microphone use</string>

```

### Add the following has a view (example)

```swift
import Zoom_Liveliness

struct ContentView: View {
    @State private var isRecording = false

    var body: some View {
        NavigationView {
            VStack {
                NavigationLink(destination: ZoomLiveliness(baseUrl: "BASE_URL", token: "USER_TOKEN", onComplete: { result in
                    // Handle the completion
                })) {
                    Text("Go to Zoom Liveliness")
                }
            }
            .navigationBarTitle("Demo")
        }
    }
}
```