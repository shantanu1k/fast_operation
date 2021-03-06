[![pub package](https://img.shields.io/pub/v/fast_operation.svg)](https://pub.dev/packages/fast_operation)

# Getting started

A dart package for conversion of various units:

- base
- angle
- distance
- temperature
- weight


## Install

Add this to your pubspec.yaml file:

```yaml
dependencies:
  fast_operation: #latest version
```

## Usage

```dart
import 'package:fast_operation/fast_operation.dart';
void main(){
  var miles = 3.12;
  var meter = Distance().convert(value: miles, from: DISTANCE.miles, to: DISTANCE.meter);
  print(meter);   //5021.15328
}
```
Each property has its own class name and a ```convert``` function:
- distance - Distance()
- weight - Weight()
- and so on

While using ```from``` and ```to```, just type ```PROPERTY``` in caps and use ```.``` to access its units.

E.g.

```dart
  var meter = Distance().convert(value: miles, from: DISTANCE.miles, to: DISTANCE.meter);
```

Here, only exception is for 'base'.
To change base between Decimal, Binary, Octal, Hexadecimal:

```dart
  var decimal = 123;
  var binary = BaseConverter().decimalToBinary(decimal);
```
