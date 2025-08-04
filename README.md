# E-Commerce Analytics Dashboard

A modern, responsive analytics dashboard built with HTML, CSS, and JavaScript that simulates real-time e-commerce data visualization.

## Features

- **Real-time Analytics**: Simulated real-time data streams with live updates
- **Interactive Charts**: Sales trends and traffic sources using Chart.js
- **Live Clickstream**: Real-time user activity feed with filtering
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Dark Theme**: Modern dark UI with excellent contrast
- **Session Drill-down**: Click on session IDs to see detailed user journeys

## Key Components

### KPI Cards
- Active Users (real-time simulation)
- Sales Today (from simulated Supabase data)
- Clicks Today (real-time tracking)
- New Orders Today (from simulated Supabase data)

### Charts
- **Sales Trends**: Line chart showing sales over time
- **Traffic Sources**: Doughnut chart showing traffic breakdown

### Real-time Features
- **Live Clickstream**: Simulated user events every 2 seconds
- **Event Filtering**: Filter by event type (page views, product views, etc.)
- **Session Tracking**: Click on session IDs to see detailed user journeys

## Data Sources (Simulated)

- **Supabase**: Sales data, traffic data, KPIs, products, and alerts
- **Kafka/WebSocket**: Real-time user events and active user count

## Getting Started

1. Open `index.html` in a modern web browser
2. The dashboard will automatically start loading data and simulating real-time events
3. Use the time range filter to switch between different time periods
4. Click on session IDs in the clickstream to see detailed user journeys
5. Use the event filters to show/hide specific event types

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Customization

### Adding Real Data Sources

To connect real data sources, replace the simulated functions:

1. **Supabase Integration**:
   ```javascript
   // Replace fetchFromSupabase function with real Supabase client calls
   const { data, error } = await supabase.from('sales').select('*')
   ```

2. **Real-time WebSocket**:
   ```javascript
   // Replace simulateKafkaStream with real WebSocket connection
   const socket = new WebSocket('wss://your-realtime-service.com')
   ```

### Styling

The dashboard uses CSS custom properties for easy theming. Modify the `:root` variables in the CSS to change colors and styling.

## File Structure

```
├── index.html          # Main dashboard file
├── README.md          # This file
└── (external CDN resources)
    ├── Font Awesome    # Icons
    └── Chart.js        # Chart library
```

## License

This project is open source and available under the MIT License.