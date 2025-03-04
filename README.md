# GitHub for Dart

![](https://github.com/SpinlockLabs/github.dart/workflows/Dart%20CI/badge.svg)
[![Pub](https://img.shields.io/pub/v/github.svg)](https://pub.dartlang.org/packages/github)

This is a Client Library for GitHub in Dart. I wrote this out of necessity, and then when I got a great reaction from the Dart community, I decided to put a lot of effort into it.

Please submit issues and pull requests, help out, or just give me encouragement.

**Notice**: We are looking for contributors. If you're interested, join us in https://gitter.im/SpinlockLabs/community

## Links

- [Library Demos](http://github.directcode.org/demos/)
- [Pub Package](https://pub.dartlang.org/packages/github)
- [Wiki](https://github.com/DirectMyFile/github.dart/wiki)

## Features

### Current

- Works on the Server and in the Browser
- Really Fast
- Plugable API
- Supports Authentication
- Builtin OAuth2 Flow
- Hook Server Helper

### Work in Progress

- Support all the GitHub APIs (Progress: 98%)

## Getting Started

First, add the following to your pubspec.yaml:

```yaml
dependencies:
  github: ^5.0.0
```

Then import the library and use it:

**For the Server**
```dart
import 'package:github/server.dart';

void main() {
  /* Creates a GitHub Client */
  var github = createGitHubClient();
  
  github.repositories.getRepository(new RepositorySlug("DirectMyFile", "github.dart")).then((Repository repo) {
    /* Do Something */
  });
}
```

**For the Browser**
```dart
import 'package:github/browser.dart';

void main() {
  /* Creates a GitHub Client */
  var github = createGitHubClient();
  
  github.repositories.getRepository(new RepositorySlug("DirectMyFile", "github.dart")).then((Repository repo) {
    /* Do Something */
  });
}
```

## Authentication

To use a GitHub token:

```dart
var github = createGitHubClient(auth: new Authentication.withToken("YourTokenHere"));
```

## Contacting Us

Join our Gitter chat at https://gitter.im/SpinlockLabs/community
