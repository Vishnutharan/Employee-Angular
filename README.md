# Employee Angular (MyAngularProject)

Angular 17 practice project using standalone components, routing and server-side rendering (SSR). It contains simple Home, About, Contact, Login and "My practice" pages, and a small in-memory service (`FakeApiServiceService`) that returns sample data as RxJS observables.

## Tech stack

- Angular 17 (standalone components) with `@angular/ssr` (Express server in `server.ts`)
- TypeScript, Bootstrap 5

## Folder structure

```text
Employee-Angular/
├── .vscode/
├── src/
│   ├── app/
│   │   ├── about/
│   │   ├── contact/
│   │   ├── home/
│   │   ├── login/
│   │   └── my-practice/
│   ├── assets/
│   ├── index.html
│   └── main.ts
├── .editorconfig
├── .gitignore
├── angular.json
├── package-lock.json
├── package.json
├── README.md
├── server.ts
├── tsconfig.app.json
├── tsconfig.json
└── tsconfig.spec.json
```

| Path | Purpose |
| --- | --- |
| `src/app/home`, `about`, `contact`, `login`, `my-practice` | Page components |
| `src/app/app.routes.ts` | Routes (`/home-componant`, `/about-componant`, `/contact-componant`, `/login-componant`, `/my-practice`) |
| `src/app/fake-api-service.service.ts` | Sample data service |
| `server.ts`, `src/main.server.ts`, `src/app/app.config.server.ts` | SSR set-up |

## Prerequisites

- Node.js 18.13+ or 20.9+ (supported by Angular 17) and npm

## Running locally

```bash
npm install
npm start                          # ng serve → http://localhost:4200
```

## Build and SSR

```bash
npm run build                      # output in dist/my-angular-project
npm run serve:ssr:my-angular-project   # serves the SSR build with Node/Express
```

## Tests

```bash
npm test                           # Karma + Jasmine
```
