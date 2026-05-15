Derived from 
[com.google.testing.platform:core-proto:0.0.9-alpha04](https://mvnrepository.com/artifact/com.google.testing.platform/core-proto/0.0.9-alpha04)

# Usage

Example after running `./gradlew connectedAndroidTest` and extracting `test-result.pb` from 
`app/build/outputs/androidTest-results/connected/<variant>/<device-id>/`:

```bash
git clone https://github.com/protocolbuffers/protobuf.git
git clone https://github.com/inthewaves/com.google.testing.platform-core-proto.git
protoc --proto_path=com.google.testing.platform-core-proto/ --proto_path=protobuf/src/ --decode=google.testing.platform.proto.api.core.TestSuiteResult com.google.testing.platform-core-proto/proto/api/core/test_suite_result.proto < test-result.pb
```
