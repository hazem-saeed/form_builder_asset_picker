# form_builder_asset_picker

Asset picker Field for [flutter_form_builder](https://pub.dev/packages/flutter_form_builder) package. Used to select files as part of form input.
It's for the web and mobile apps. Desktop wasn't tested.

This is a fork of [form_builder_file_picker](https://pub.dev/packages/form_builder_file_picker) made by Danvick Miller.

# Setup

This package makes use of [file_picker package](https://pub.dev/packages/file_picker) and [permission_handler package](https://pub.dev/packages/permission_handler). For platform specific setup, follow their instructions.

# Usage

```dart
 import 'package:flutter_form_builder/flutter_form_builder.dart';
 import 'package:form_builder_file_picker/form_builder_asset_picker.dart';

 ...

 final List<String>? _allowedExtensions = ['png', 'pdf'];

 ...

 FormBuilderAssetPicker(
    name: 'pick-file',
    allowedExtensions: _allowedExtensions,
    allowMultiple: true,
    maxFiles: 5,
    type: FileType.custom,
    decoration: const InputDecoration(border: InputBorder.none),
    selector: Row(
        children: const [
            Icon(Icons.file_upload),
            Text('Upload')
        ]
    )
 )
```

# Additional Notes

After version 7.0.0 of "flutter_form_builder", you will need to install the package "form_builder_validators" if you wish to use their form validators.