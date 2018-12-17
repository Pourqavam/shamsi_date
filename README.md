# A Flutter package for using Jalali (Shamsi, Solar or Persian) date. You can convert Jalali and Georgian dates to each other.

Converted from Javascript library hosted on: [jalaali-js](https://github.com/jalaali/jalaali-js)

## Usage

Add it to your pubspec.yaml file:

```yaml
dependencies:
    shamsi_date: ^0.2.1
```

Import and use it:

```dart
import 'package:shamsi_date/shamsi_date.dart';

main() {
  final g1 = Gregorian(2013, 1, 10);
  final j1 = g1.toJalali();
  print('$g1 in Gregorian is $j1 in Jalali');

  final j2 = Jalali(1391, 10, 21);
  final g2 = j1.toGregorian();
  print('$j2 in Jalali is $g2  in Gregorian');

  // check validity
  print('$j1 is valid? ${j1.isValid()}');

  // check leap year
  print('1390 is leap year? ${Jalali(1390).isLeapYear()}');

  // find month length
  print('1390/12 month length? ${Jalali(1390, 12).monthLength}');
}
```
