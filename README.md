# YOOM - Zoom Clone

YOOM is a modern video calling web application inspired by Zoom, built with Next.js, Clerk authentication, and Stream Video SDK. It features user authentication, personal and scheduled meeting rooms, recordings, and a responsive UI.

## Features

- **User Authentication:** Secure sign-up and sign-in using Clerk.
- **Personal Room:** Each user has a dedicated personal meeting room.
- **Schedule Meetings:** Create, view, and join upcoming meetings.
- **Previous Meetings:** Access a list of past meetings.
- **Recordings:** View and manage meeting recordings.
- **Responsive UI:** Optimized for both desktop and mobile devices.
- **Modern UI Components:** Built with Radix UI, Tailwind CSS, and custom components.
- **Video Calls:** Powered by Stream Video React SDK.

## Project Structure

```
zoom-clone-main/
  ├── app/
  │   ├── (auth)/sign-in/[[...sigin-in]]/page.tsx      # Sign-in page
  │   ├── (auth)/sign-up/[[...sign-up]]/page.tsx       # Sign-up page
  │   ├── (root)/(home)/                               # Home and dashboard
  │   │   ├── personal-room/                           # Personal meeting room
  │   │   ├── upcoming/                                # Upcoming meetings
  │   │   ├── previous/                                # Previous meetings
  │   │   ├── recordings/                              # Meeting recordings
  │   ├── (root)/meeting/[id]/page.tsx                 # Dynamic meeting room
  │   ├── layout.tsx                                   # App layout with ClerkProvider
  │   └── globals.css                                  # Global styles
  ├── components/                                      # UI and meeting components
  ├── hooks/                                           # Custom React hooks
  ├── providers/                                       # Context providers (e.g., Stream)
  ├── constants/                                       # App constants
  ├── lib/                                             # Utility functions
  ├── middleware.ts                                    # Route protection with Clerk
  ├── package.json                                     # Project dependencies and scripts
  └── README.md                                        # Project documentation
```

## Tech Stack

- **Framework:** [Next.js](https://nextjs.org/)
- **Authentication:** [Clerk](https://clerk.com/)
- **Video SDK:** [Stream Video React SDK](https://getstream.io/video/)
- **UI:** [Radix UI](https://www.radix-ui.com/), [Tailwind CSS](https://tailwindcss.com/)
- **Date Handling:** [date-fns](https://date-fns.org/)
- **Icons:** [Lucide React](https://lucide.dev/)

## Getting Started

### Prerequisites

- Node.js v18 or higher
- npm

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/zoom-clone-main.git
   cd zoom-clone-main/zoom-clone-main
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env.local` file in the root directory and add your Clerk keys:

   ```
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key
   ```

   > Get your keys from the [Clerk dashboard](https://dashboard.clerk.com/).

4. **Run the development server:**

   ```bash
   npm run dev
   ```

   The app will be available at [http://localhost:3000](http://localhost:3000).

### Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build for production
- `npm run start` - Start the production server
- `npm run lint` - Lint the codebase

## Folder Highlights

- **components/**: Reusable UI and meeting components (e.g., Navbar, MeetingRoom, Loader).
- **hooks/**: Custom hooks for fetching calls and call details.
- **providers/**: Context providers, such as StreamClientProvider.
- **app/(auth)/**: Authentication pages using Clerk.
- **app/(root)/(home)/**: Main dashboard, personal room, upcoming/previous meetings, and recordings.
- **app/(root)/meeting/[id]/**: Dynamic meeting room pages.

## Authentication & Security

- All main routes are protected using Clerk middleware.
- Only authenticated users can access meetings, recordings, and personal rooms.

## Customization

- Easily customize the UI via Tailwind CSS and Radix UI components.
- Update branding by changing icons and colors in `app/layout.tsx`.

