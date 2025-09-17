# Van Der Sinn Band Website

## Overview

Van Der Sinn is a full-stack web application for a music band's official website. The application showcases the band's discography, member information, collaborations, and provides functionality for booking inquiries. It features a vintage-inspired design with modern web technologies, combining analog aesthetics with digital precision to match the band's musical philosophy.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The frontend is built with React 18 and TypeScript, using Vite as the build tool. The application follows a component-based architecture with:

- **Routing**: Wouter for client-side routing with pages for home, album details, and 404 handling
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Framework**: Radix UI components with shadcn/ui design system for consistent, accessible components
- **Styling**: Tailwind CSS with custom CSS variables for theming, featuring a vintage/retro aesthetic with custom fonts (Bodoni Moda, Playfair Display, Inter)
- **Form Handling**: React Hook Form with Zod validation for type-safe form management

### Backend Architecture
The backend uses Express.js with TypeScript in ESM format:

- **API Design**: RESTful API structure with routes for albums, band members, collaborations, and booking inquiries
- **Request Handling**: Express middleware for JSON parsing, URL encoding, and request logging
- **Error Handling**: Centralized error handling middleware with proper HTTP status codes
- **Development Setup**: Hot reloading with tsx and Vite integration for seamless development experience

### Data Storage Solutions
The application uses a hybrid storage approach:

- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Development Storage**: In-memory storage implementation (MemStorage) with seeded data for development
- **Schema Management**: Shared TypeScript schema definitions with Zod validation for runtime type checking
- **Database Provider**: Neon Database serverless PostgreSQL for production deployment

### Component Structure
The frontend is organized into reusable components:

- **Layout Components**: Navigation, Footer, Hero sections
- **Content Sections**: Releases gallery, band information, collaborations, recording process
- **Interactive Components**: Booking form, Bandcamp player integration
- **UI Components**: Complete set of accessible UI components from shadcn/ui

### Build and Deployment
- **Development**: Vite dev server with HMR and error overlay
- **Production Build**: Vite for frontend bundling, esbuild for backend compilation
- **Static Assets**: Public folder structure for images and static content
- **Environment Configuration**: Environment-based configuration for database and API endpoints

## External Dependencies

### Database Services
- **Neon Database**: Serverless PostgreSQL database with connection pooling
- **Drizzle ORM**: Type-safe database toolkit with schema migrations

### Frontend Libraries
- **TanStack Query**: Server state management and caching
- **Wouter**: Lightweight client-side routing
- **React Hook Form**: Form state management and validation
- **Zod**: Runtime type validation and schema definition
- **Radix UI**: Accessible component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library

### Development Tools
- **Vite**: Fast build tool with HMR support
- **TypeScript**: Static type checking across the full stack
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Autoprefixer

### Third-party Integrations
- **Bandcamp**: Music streaming and player embeds for album previews
- **Google Fonts**: Custom typography (Bodoni Moda, Playfair Display, Inter)
- **Unsplash/Pixabay**: Stock photography for album covers and band images

### Session Management
- **connect-pg-simple**: PostgreSQL session store for user session management
- **Express Session**: Server-side session handling middleware

The architecture prioritizes type safety, developer experience, and maintainable code while delivering a performant user experience that reflects the band's aesthetic vision of combining vintage warmth with modern precision.