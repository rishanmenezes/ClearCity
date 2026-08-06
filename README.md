# ClearCity - Real-Time Urban Pollution Tracker

A comprehensive web application for tracking air quality worldwide with real-time data visualization, interactive maps, and community engagement features.

## 🌟 Project Overview

ClearCity is a modern React-based application that provides real-time air quality monitoring for cities around the world. Users can view current air quality data, historical trends, forecasts, and access detailed information about pollutants through an intuitive interface.

## 🚀 Features

### Core Functionality
- **Interactive Air Quality Map**: Leaflet-powered map for exploring air quality data globally
- **Real-Time Data**: Current air quality measurements via OpenWeatherMap API
- **Historical Analysis**: 24-hour historical air quality data visualization
- **Forecast Data**: Predictive air quality information
- **City Search**: Search functionality for 25+ major cities worldwide
- **Detailed Pollutant Information**: Breakdown of PM2.5, PM10, O₃, NO₂, SO₂, CO, and NH₃ levels
- **AQI Index**: Color-coded Air Quality Index (1-5 scale) with health implications

### Additional Features
- **City Guides**: Detailed information about common pollutants, health tips, and environmental regulations for major cities
- **Community Ideas**: Platform for sharing and discussing air quality improvement solutions
- **AI Chatbot**: Interactive chatbot with FAQ about air quality and app usage
- **Data Visualization**: Recharts-powered graphs for air quality trends
- **Responsive Design**: Mobile-friendly interface with Tailwind CSS

## 🛠️ Technology Stack

### Frontend Framework
- **React 18.3.1**: UI library with hooks and modern React patterns
- **TypeScript 5.5.3**: Type-safe development
- **Vite 5.4.19**: Fast build tool and dev server

### UI Components & Styling
- **shadcn/ui**: Pre-built React components with Radix UI primitives
- **Tailwind CSS 3.4.11**: Utility-first CSS framework
- **Radix UI**: Accessible component primitives
  - Dialog, Dropdown Menu, Tabs, Progress, Scroll Area, Select, etc.
- **Lucide React**: Icon library
- **class-variance-authority**: Component variant management
- **clsx & tailwind-merge**: Conditional class management

### Data & State Management
- **@tanstack/react-query 5.56.2**: Data fetching and caching
- **React Hook Form 7.53.0**: Form management with Zod validation
- **Zod 3.23.8**: Schema validation

### Maps & Visualization
- **Leaflet 1.9.4**: Interactive maps
- **react-leaflet 4.2.1**: React integration for Leaflet
- **Recharts 2.12.7**: Chart library for data visualization

### Routing & Navigation
- **react-router-dom 6.26.2**: Client-side routing

### Utilities
- **date-fns 3.6.0**: Date formatting and manipulation
- **sonner 1.5.0**: Toast notifications

### Development Tools
- **ESLint 9.9.0**: Code linting
- **TypeScript ESLint 8.0.1**: TypeScript-specific linting
- **PostCSS 8.4.47**: CSS processing
- **Autoprefixer 10.4.20**: CSS vendor prefixing

## 📁 Project Structure

```
Clear City/
├── public/                      # Static assets
│   ├── favicon.ico
│   ├── placeholder.svg
│   └── robots.txt
├── src/
│   ├── components/             # React components
│   │   ├── ui/                # shadcn/ui components (45+ components)
│   │   ├── AirQualityChart.tsx
│   │   ├── AirQualityMap.tsx
│   │   ├── ApiKeyForm.tsx
│   │   ├── AqiCard.tsx
│   │   ├── AqiIndex.tsx
│   │   ├── Chatbot.tsx
│   │   ├── CitySearch.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Header.tsx
│   │   └── PollutantInfo.tsx
│   ├── contexts/              # React Context providers
│   │   └── ApiKeyContext.tsx
│   ├── hooks/                 # Custom React hooks
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   ├── lib/                   # Utility functions
│   │   └── utils.ts
│   ├── pages/                 # Page components
│   │   ├── About.tsx
│   │   ├── CityGuide.tsx
│   │   ├── CommunityIdeas.tsx
│   │   ├── Index.tsx
│   │   └── NotFound.tsx
│   ├── services/              # API services
│   │   └── airQualityService.ts
│   ├── types/                 # TypeScript type definitions
│   │   └── airQuality.ts
│   ├── App.tsx                # Main app component
│   ├── index.css              # Global styles
│   ├── main.tsx               # Application entry point
│   └── vite-env.d.ts          # Vite type definitions
├── .gitignore
├── .npmrc
├── components.json            # shadcn/ui configuration
├── eslint.config.js           # ESLint configuration
├── index.html                 # HTML template
├── package.json               # Dependencies and scripts
├── postcss.config.js          # PostCSS configuration
├── tailwind.config.js         # Tailwind CSS configuration
├── tailwind.config.ts         # Tailwind TypeScript configuration
├── tsconfig.json              # TypeScript configuration
├── tsconfig.app.json          # App-specific TypeScript config
├── tsconfig.node.json         # Node-specific TypeScript config
└── vite.config.ts             # Vite configuration
```

## 📄 Component Details

### Main Components

#### Dashboard (`Dashboard.tsx`)
- Central hub for air quality monitoring
- Integrates map, city search, and data visualization
- Manages state for selected locations and air quality data
- Handles historical and forecast data queries

#### AirQualityMap (`AirQualityMap.tsx`)
- Leaflet-based interactive map component
- Click-to-fetch air quality data for any location
- Custom markers with AQI color coding
- Reverse geocoding for location names

#### CitySearch (`CitySearch.tsx`)
- Search functionality with auto-complete
- Pre-loaded with 25+ popular cities
- API integration for dynamic city lookup
- Dropdown suggestions and popular city buttons

#### ApiKeyForm (`ApiKeyForm.tsx`)
- Secure API key input with validation
- Form validation using Zod schema
- LocalStorage persistence for API keys
- Integration with OpenWeatherMap API validation

#### Chatbot (`Chatbot.tsx`)
- AI-powered assistant with FAQ database
- Context-aware responses based on current air quality data
- Comprehensive knowledge base about pollutants and health
- Interactive message interface with typing indicators

### Page Components

#### Index (`Index.tsx`)
- Landing page with API key authentication
- Conditional rendering based on API key validity
- Chatbot integration and floating action button

#### CityGuide (`CityGuide.tsx`)
- Detailed city-specific air quality information
- Health tips and environmental regulations
- Tabbed interface for different information categories
- City-specific pollutant data

#### CommunityIdeas (`CommunityIdeas.tsx`)
- Community engagement platform
- Idea submission with categorization
- Like and comment functionality
- Category-based filtering and sorting

#### About (`About.tsx`)
- Project information and team details
- Feature descriptions and technology overview
- Team member profiles

### Supporting Components

#### AqiCard (`AqiCard.tsx`)
- Displays current air quality metrics
- Color-coded AQI badge
- Pollutant concentration display (PM2.5, PM10, O₃, NO₂)

#### PollutantInfo (`PollutantInfo.tsx`)
- Detailed pollutant breakdown with progress bars
- Threshold-based color coding
- Health risk indicators

#### AirQualityChart (`AirQualityChart.tsx`)
- Recharts-based line charts
- Historical and forecast data visualization
- Multi-pollutant tracking
- Responsive design with tooltips

#### Header (`Header.tsx`)
- Navigation bar with routing
- Responsive design with interactive buttons
- Gradient styling and hover effects

## 🔧 Configuration Files

### Vite Configuration (`vite.config.ts`)
- React SWC plugin for fast React compilation
- Path aliases (@/* for src/*)
- Development server configuration (port 8080)
- Component tagger for development mode

### Tailwind Configuration (`tailwind.config.ts`)
- Custom color scheme with CSS variables
- Dark mode support
- Custom animations (fade-in, scale-in, float, pulse-gentle)
- Extended box shadows and border radius
- Custom utility classes for interactive elements

### TypeScript Configuration
- Strict mode disabled for flexibility
- Path aliases configured
- Separate configs for app and node environments
- Comprehensive type checking with relaxed rules

### ESLint Configuration
- TypeScript ESLint with recommended rules
- React Hooks and React Refresh plugins
- Custom rules for unused variables
- Ignored directories (dist, node_modules)

## 🌐 API Integration

### OpenWeatherMap API
The application uses the OpenWeatherMap API for:
- **Current Air Quality**: `/air_pollution` endpoint
- **Forecast Data**: `/air_pollution/forecast` endpoint
- **Historical Data**: `/air_pollution/history` endpoint
- **Geocoding**: `/geo/1.0/direct` endpoint for city lookup

### Data Models
- **AirQualityData**: Response structure for air quality API
- **AirQualityItem**: Individual air quality measurement
- **City**: City coordinate information
- **AirQualityLevels**: AQI classification system (1-5 scale)

## 🎨 Styling Approach

### Design System
- **Color Palette**: Purple primary theme with semantic colors for AQI levels
- **Typography**: System fonts with responsive sizing
- **Spacing**: Tailwind's spacing scale with custom utilities
- **Animations**: Custom keyframe animations for smooth transitions
- **Dark Mode**: Full dark mode support via CSS variables

### Custom CSS
- Leaflet map popup styling
- AQI card custom shadows
- Interactive button effects
- Custom scrollbar styling
- Toast notification animations

## 🔐 Authentication

### API Key Management
- Client-side API key validation
- LocalStorage persistence
- Context-based state management
- Form validation with Zod schemas
- Error handling with toast notifications

## 📱 Responsive Design

### Breakpoints
- Mobile: Default styles
- Tablet: md: breakpoint (768px)
- Desktop: lg: breakpoint (1024px)
- Large Desktop: 2xl: breakpoint (1400px)

### Mobile Considerations
- Touch-friendly interface
- Responsive map sizing
- Collapsible navigation
- Optimized component layouts

## 🚦 Available Scripts

```bash
# Development server with hot reload
npm run dev

# Production build
npm run build

# Development build
npm run build:dev

# Lint code
npm run lint

# Preview production build
npm run preview
```

## 🌍 Supported Cities

### Americas
New York, Los Angeles, Mexico City, Toronto, São Paulo

### Europe
London, Paris, Berlin, Rome, Madrid

### Asia
Tokyo, Beijing, Mumbai, Seoul, Bangkok

### India (Special Focus)
Delhi, Bengaluru, Chennai, Kolkata, Hyderabad, Mysuru

### Africa
Cairo, Lagos, Nairobi, Cape Town

### Oceania
Sydney, Melbourne, Auckland

## 🎯 AQI Index System

### Scale (1-5)
1. **Good** (Green): Air quality satisfactory, little or no risk
2. **Moderate** (Yellow): Acceptable quality, minor concerns for sensitive groups
3. **Unhealthy for Sensitive Groups** (Orange): Health effects for sensitive individuals
4. **Unhealthy** (Red): Everyone may experience health effects
5. **Very Unhealthy** (Purple): Health alert, serious effects for everyone

### Tracked Pollutants
- **PM2.5**: Fine particulate matter (μg/m³)
- **PM10**: Coarse particulate matter (μg/m³)
- **O₃**: Ozone (μg/m³)
- **NO₂**: Nitrogen dioxide (μg/m³)
- **SO₂**: Sulfur dioxide (μg/m³)
- **CO**: Carbon monoxide (μg/m³)
- **NH₃**: Ammonia (μg/m³)

## 👥 Team

- **Rishan**: Environmental data analysis and visualization
- **Keerthi**: Frontend development and user experience design
- **Sathish**: Data integration and API development
- **Chinmay**: Community engagement features and documentation

## 📝 Development Notes

### Key Patterns
- React Query for data fetching and caching
- Context API for global state management
- Custom hooks for reusable logic
- TypeScript for type safety
- Component composition with shadcn/ui

### Performance Optimizations
- Code splitting with React.lazy
- Image optimization
- Efficient re-renders with React.memo
- Debounced search inputs
- Virtual scrolling for large lists

### Error Handling
- Try-catch blocks for API calls
- User-friendly error messages with toast notifications
- Fallback UI for failed data loads
- Form validation with clear error messages

## 🔮 Future Enhancements

Potential areas for expansion:
- User authentication and saved locations
- Push notifications for air quality alerts
- Historical data analysis and trends
- Multi-language support
- Additional air quality APIs integration
- Mobile app development
- Real-time websocket updates

## 📄 License

This project was generated with Lovable and uses open-source libraries with their respective licenses.

## 🤝 Contributing

To contribute to this project:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📧 Support

For issues or questions about the ClearCity application, please refer to the project documentation or contact the development team.
