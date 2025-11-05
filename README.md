# 📱 Todo React Native App

![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## ✨ Introduction
Welcome to **Todo React Native**! This repository is based on the latest Expo Router and React Native template, designed as a starter for a cross-platform, modern TODO/task management app using TypeScript and Expo.

---

## 🏗️ App Architecture

**Folder Structure**
```
/
├── app/            # App entrypoint & navigation (Expo Router)
│   ├── (tabs)/     # Main tab navigation (index.tsx, explore.tsx, _layout.tsx)
│   ├── +not-found.tsx
│   └── _layout.tsx
├── components/     # Shared React Native UI components
├── constants/      # Constants (e.g., Colors.ts)
├── hooks/          # Custom React hooks (e.g., useColorScheme)
├── scripts/        # Utility scripts
├── assets/         # Images & static files
├── package.json
```

**Component Breakdown**:
- `components/ui/`, `Collapsible.tsx`, `ParallaxScrollView.tsx`, etc.: Individual presentation components
- `hooks/`: Custom theming and color scheme logic
- Navigation handled with Expo Router (`app/(tabs)/_layout.tsx`)
- Screens are under `app/(tabs)/` (currently `index.tsx`, `explore.tsx`)

---

## 🌟 Core Features (Current State)
- Cross-platform Expo project setup (iOS/Android/Web)
- TypeScript throughout the codebase
- Customizable theming
- Expo Router navigation template
- Modern UI structure ready for expansion

> **Note:** The actual TODO/business logic is **not yet implemented** — this project currently serves as a technical scaffold for a TODO app.

---

## ⚙️ API/Logic Explanation
At present:
- No external APIs or persistent business logic is present
- The custom hooks in `hooks/` (`useColorScheme`, `useThemeColor`) handle dynamic theming
- No usage of AsyncStorage yet (to be implemented)
- Example UI logic is present in components like `HelloWave`, `Collapsible`, and navigation layouts

---

## 🚦 Example Usage
Example: How to use a custom color hook inside a component:
```tsx
import { useThemeColor } from '../hooks/useThemeColor';

export default function MyComponent() {
  const color = useThemeColor({}, 'text');
  return <Text style={{ color }}>Hello!</Text>;
}
```

Example: Adding a new screen (under `app/(tabs)/`):
```tsx
// app/(tabs)/profile.tsx
import { Text } from 'react-native';
export default function ProfileScreen() {
  return <Text>Profile</Text>;
}
```

---

## 🧪 Test Coverage
- As of now, **no test suites** are implemented.
- To add tests: Scaffold with [Jest](https://jestjs.io/) or [React Native Testing Library](https://testing-library.com/docs/react-native-testing-library/intro/).

---

## 🚀 Performance Optimizations
- Expo + TypeScript ensures robust build-time/type-time validation
- Minimalistic project setup for fast iteration
- Utilizes React Native's built-in optimizations

---

## ⏳ Limitations / TODOs
- **Core TODO logic not implemented:** No create/edit/delete task features yet
- **No state management:** Redux/MobX/Zustand, etc., are not included
- **No persistent storage:** AsyncStorage or remote backend not in use
- **No API integration implemented**
- **No automated tests**

**Planned Improvements:**
- Implement task model, persistent storage, and editing/deleting features
- Add state management for scalable data flows
- Add proper test coverage
- Implement example REST/GraphQL API integration

---

## 📦 Installation & Usage

### Prerequisites
- Node.js v18+
- npm or yarn
- Expo CLI (recommended)

```sh
git clone https://github.com/Karthikeyan-BE/Todo_ReactNative.git
cd Todo_ReactNative
npm install   # or yarn install
npx expo start
```

Open on iOS/Android using Expo Go or with a local simulator.

---

## 🤝 Contributing
See [CONTRIBUTING](CONTRIBUTING.md) for guidelines, or open an issue with your proposal/bug.

---

## 📄 License
MIT — see [LICENSE](LICENSE).

---

_Made with Expo and React Native._
