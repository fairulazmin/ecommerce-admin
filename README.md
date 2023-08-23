This is a [E-Commerce](https://www.youtube.com/watch?v=5miHyP6lExg&t=417s) project based on [Code with Antonio](https://www.youtube.com/@codewithantonio) Youtube channel.

## Installation

Create a project

```
npx create-next-app@latest ecommerce-admin --typescript --tailwind --eslint
```

Run the [shadcn-ui](https://ui.shadcn.com/docs/installation/next) init command to setup the project
```
npx shadcn-ui@latest init
```

Install [Clerk](https://clerk.com/docs/quickstarts/nextjs) for authentification
```
npm install @clerk/nextjs
```

Install [Prisma](https://www.prisma.io/docs/getting-started/setup-prisma/add-to-existing-project/relational-databases-typescript-mysql)
```
npm i -D prisma
npm i @prisma/client
npx prisma init
```

Create database with [PlanetScale](https://planetscale.com/docs/prisma/prisma-quickstart)

## Configuration
Edit `app/global.css`, add...
```
html,
body,
:root{
  height: 100%;
}
```

File structure
```
|--app
   |--(auth)
   |  |--(routes)
   |  |  |--sign-in
   |  |  |  |--[[...sign-in]]
   |  |  |     |--page.tsx
   |  |  |--sign-up
   |  |     |--[[...sign-up]]
   |  |        |--page.tsx
   |  |--layout.tsx
   |--(root)
      |--page.tsx
```

Add `.env` file
```
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY={{pub_key}}
CLERK_SECRET_KEY={{secret}}
```

Edit the `.gitignore` file
```
.env
```
