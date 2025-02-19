# Pathway 1-2

- **Jetpack Compose 단계**
    - [https://developer.android.com/jetpack/compose/phases](https://developer.android.com/jetpack/compose/phases)
- **상태 및 Jetpack Compose**
    - [https://developer.android.com/jetpack/compose/state](https://developer.android.com/jetpack/compose/state)

## Compose 기본 사항

- Compose Phases
    
<img width="811" alt="1" src="https://user-images.githubusercontent.com/87517193/204217531-0c88f0ca-bb2d-4b0b-ad2a-219ee129b4a5.png">

    
- Recomposition
    - 이미 작업이 끝난 Composable 함수에 대해서 Composition 단계부터 새로 수행하는 것
    - Smart Recomposition
        - Recomposition이 필요 없는 부분은 갱신되지 않는다.
    
<img width="789" alt="2" src="https://user-images.githubusercontent.com/87517193/204217563-db7b4dd6-fdfc-49df-877f-a84ffbfe83bb.png">

    
- State in Composition
    - State, MutableState
        - Value Holder, Observable, Recomposition Trigger
    - Remember로 Recomposition시 값을 유지하게 해야함
    - Stateful vs Stateless
    - Stateless가 권장됨
        - Single source of truth
        - Encapsulated
        - Decoupled - State로부터 자유롭기 때문에 독립적으로 쓸 수 있어서 재사용성이 높다.
    - State Hoisting
        - 재사용성을 높이는 과정
        - 호출자 쪽에서 State를 관리하도록 코드를 짜는 것
        - [https://kotlinworld.com/244](https://kotlinworld.com/244)
- CompositionLocal
    - `CompositionLocalProvider(LocalColor provides color) {}`
    - [https://developer.android.com/jetpack/compose/compositionlocal?hl=ko](https://developer.android.com/jetpack/compose/compositionlocal?hl=ko)
- Compose Theming
    - MaterialTheme
