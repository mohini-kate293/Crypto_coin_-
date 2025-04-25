# Crypto Dashboard

A modern, real-time cryptocurrency dashboard built with React, Redux, and WebSockets.

![Crypto Dashboard](https://i.imgur.com/JBtYYHB.png)

## Features

- **Real-Time Updates**: Live price updates via WebSockets from Binance
- **7-Day Charts**: Visual representation of price movements over the past week
- **Detailed Information**: Comprehensive data for each cryptocurrency
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Live Search**: Filter cryptocurrencies in real-time
- **Sorting**: Sort by any column (price, market cap, etc.)
- **Animated UI**: Smooth animations using Framer Motion
- **State Management**: Robust Redux architecture

## Technologies Used

- **React 19**: For building the UI
- **Redux Toolkit**: For state management
- **WebSockets**: For real-time data updates
- **Tailwind CSS**: For styling
- **Framer Motion**: For animations
- **Vite**: For fast development and production builds

## Getting Started

### Prerequisites

- Node.js 16+ installed
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/crypto-dashboard.git
cd crypto-dashboard
```

2. Install dependencies
```bash
npm install
# or
yarn
```

3. Start the development server
```bash
npm run dev
# or
yarn dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Usage

- **View Crypto Prices**: The main page displays a list of popular cryptocurrencies with their current prices and changes
- **Sort Data**: Click on any column header to sort by that field
- **Search Coins**: Use the search box to filter cryptocurrencies
- **See Details**: Click on any row to open a detailed view of that cryptocurrency
- **Real-Time Updates**: Watch prices update in real-time with color indicators for price movements

## Project Structure

```
src/
├── app/
│   └── store.js          # Redux store configuration
├── assets/               # Static assets
├── features/
│   └── crypto/           # Crypto feature
│       ├── CoinChart.jsx # 7-day chart component
│       ├── CoinDetail.jsx # Detailed view component
│       ├── CryptoList.jsx # Main list component
│       ├── cryptoSlice.js # Redux slice for crypto data
│       └── WebSocketProvider.jsx # WebSocket manager
├── utils/
│   └── websocketService.js # WebSocket service
├── App.jsx                # Main app component
└── main.jsx               # Entry point
```

## WebSocket Implementation

The application connects to Binance's WebSocket API to receive real-time updates for cryptocurrency prices. If the WebSocket connection fails, it will fall back to polling the CoinGecko API every 60 seconds.

## Redux State Management

Redux is used to manage the application state, with actions for:
- Fetching initial price data
- Updating prices via WebSocket
- Tracking WebSocket connection status
- Managing selected coins

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Data provided by CoinGecko API and Binance WebSocket API
- Chart images from CoinMarketCap
