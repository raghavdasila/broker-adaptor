# Broker Adaptor

A Next.js 16 project with App Router and TypeScript.

## Features

- **Next.js 16** with App Router
- **TypeScript** for type safety
- **Tailwind CSS** for styling
- **ESLint** for code quality (manual execution only)

## Build Configuration

This project is configured to **skip linting and warning checks during build**:

### TypeScript Type Checking
TypeScript type checking is disabled during production builds via the `next.config.ts` configuration:

```typescript
typescript: {
  ignoreBuildErrors: true,
}
```

This means `next build` will complete successfully even if there are TypeScript errors in the code. The build process will show "Skipping validation of types" message.

### ESLint
In Next.js 16, ESLint does not run automatically during `next build`. ESLint is only executed when you explicitly run:

```bash
npm run lint
```

This separation ensures that the build process is fast and doesn't fail due to linting issues.

## Getting Started

### Install Dependencies

```bash
npm install
```

### Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

### Production Build

```bash
npm run build
```

The build will complete successfully even if there are TypeScript errors or ESLint warnings.

### Start Production Server

```bash
npm start
```

### Linting (Optional)

To manually check for linting issues:

```bash
npm run lint
```

## Project Structure

- `/src/app` - App Router pages and layouts
- `/public` - Static assets
- `next.config.ts` - Next.js configuration (includes build settings)
- `tsconfig.json` - TypeScript configuration
- `eslint.config.mjs` - ESLint configuration

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
