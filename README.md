## [flutter] 핫리로드

- `build() {}` 안에 있는 코드만 핫리로드 된다. 

## [flutter] 로딩 인디케이터 (아이콘)

```dart
class SplashScreen extends StatelessWidget {
  const SplashScreen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Container(
      color: const Color(0xffFA9231),
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Image.asset('assets/img/logo.png'),
          const CircularProgressIndicator(
            color: Colors.white,
          ),
        ],
      ),
    );
  }
}
```

## 시뮬레이터에 debug 디버그 플래그 없애기

- `debugShowCheckedModeBanner` 속석을 `false` 로 변경

```dart
void main() {
  runApp(
    const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: SplashScreen(),
      ),
    )
  );
}
```