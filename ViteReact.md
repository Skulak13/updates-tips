# 🧠 React Compiler – co warto wiedzieć (2025)

## 🧩 Co to właściwie jest „React Compiler”

**React Compiler** to nowy, oficjalny kompilator Reacta (część projektu **React 19+**).  
Jego celem jest **automatyczne optymalizowanie komponentów** — czyli usuwa potrzebę ręcznego używania:

- `React.memo`
- `useCallback`
- `useMemo`

Działa **bez zmiany składni JSX**, więc wszystkie kody Reacta generowane przez AI są nadal **poprawne ✅**.  
Różnice występują „pod maską” (w sposobie kompilacji), a nie w sposobie pisania kodu.

---

## ⚙️ Co AI (i ty) musisz wiedzieć, żeby wszystko działało

Aby AI generowało kod w pełni zgodny z twoim setupem, dodaj krótką adnotację w promptach:

> 💬 „Używam Vite + React + TypeScript + React Compiler.  
> Pisz kod kompatybilny z React 19, bez niepotrzebnego `memo`, `useCallback` itp.”

Dzięki temu unikniesz sytuacji, w której AI dorzuca stare optymalizacje, które nie są już potrzebne.

---

## 📋 Co działa tak samo jak wcześniej

Wszystkie standardowe rzeczy Reacta działają dokładnie tak samo:

- JSX  
- `useState`, `useEffect`, `useRef`, `useContext`  
- **Framer Motion**  
- **React Router**  
- **Tailwind CSS**  
- **Matter.js**  
- **requestAnimationFrame**

---

## ⚠️ Co może wymagać uwagi

- **Starsze biblioteki** (nieaktualizowane od 2+ lat) mogą nie być testowane z React Compilerem —  
  ale w praktyce nadal działają, bo API Reacta się nie zmieniło.  
- Niektóre tutoriale online (np. z 2022–2023) będą mówiły:  
  > „Użyj `useMemo` lub `React.memo`, żeby poprawić wydajność.”  
  — tego już **nie musisz robić**, bo React Compiler zrobi to automatycznie.  
- Jeśli używasz **React Server Components (RSC)**, konfiguracja może być bardziej złożona,  
  ale Vite + React Compiler działa po stronie klienta, więc jesteś bezpieczny.

---

## 💡 Pro tip

Na początku projektu możesz dodać komentarz w głównym pliku (`App.tsx`):

```tsx
// Project setup: Vite + React + TypeScript + React Compiler (React 19)
// No need for manual memoization (React.memo, useCallback, useMemo)

## ✅ Podsumowując

| Aspekt | React Compiler (TypeScript + React Compiler) | Klasyczny React |
|--------|----------------------------------------------|-----------------|
| **Zgodność z AI promptami** | ✅ pełna | ✅ pełna |
| **Potrzeba `useMemo`, `React.memo`** | 🚫 nie | ✅ tak |
| **Wydajność** | ⚡ wyższa automatycznie | dobra, ale ręczna optymalizacja |
| **Nowoczesność stacku** | 🔥 najnowszy (2025) | klasyczny |
| **Stabilność bibliotek** | ✅ w 95% zgodne | ✅ w 100% |
