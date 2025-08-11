# TabRow with HorizontalPager in Jetpack Compose

This sample demonstrates how to implement a `TabRow` with icons and text, fully synchronized with a `HorizontalPager` using the new [`foundation.pager`](https://developer.android.com/reference/kotlin/androidx/compose/foundation/pager/package-summary) API in Jetpack Compose.

## Features
- **Tab navigation** with selected/unselected icons and text.
- **HorizontalPager** integration with smooth animations.
- **State synchronization** between selected tab and current page using `derivedStateOf`.
- **Material 3** layout with `Scaffold` and `TopAppBar`.
- **Enum-based tab definitions** for clean and maintainable code.

## Screenshots
> *(Add your screenshot here)*
>
> ![Screenshot Placeholder](docs/screenshot.png)

## How It Works
- Tabs are defined in the `HomeTabs` enum, each with a selected icon, unselected icon, and label.
- `rememberPagerState` manages the pager’s current page count and state.
- `TabRow` listens to `pagerState.currentPage` via `derivedStateOf` to highlight the active tab.
- On tab click, `animateScrollToPage` is triggered using `rememberCoroutineScope` for smooth scrolling.
- The pager displays content for each tab and updates automatically when swiped.
