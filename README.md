# DeFi Opportunity Checker 🚀

A Node-RED based DeFi yield optimization dashboard that monitors and analyzes lending and liquidity pool opportunities across major DeFi protocols.

## 🎯 Overview

This project provides a real-time DeFi opportunity analyzer that helps users identify the best yield farming opportunities by:
- Fetching live yield data from DeFiLlama's API
- Comparing opportunities against your current portfolio
- Calculating potential improvements and annual gains
- Providing risk scoring and smart warnings
- Generating AI-powered insights using OpenAI GPT

## ✨ Features

### Core Functionality
- **Real-time Yield Monitoring**: Fetches current APY data from major DeFi protocols
- **Portfolio Tracking**: Maintains user-specific portfolio positions
- **Smart Ranking**: Ranks opportunities by improvement potential and risk score
- **Risk Assessment**: Evaluates opportunities based on TVL, APY sustainability, and protocol reputation
- **AI Analysis**: Generates intelligent insights and recommendations using OpenAI
- **User Authentication**: Secure login system with user-specific portfolios
- **Responsive Dashboard**: Clean, modern interface with real-time updates

### Supported Protocols
- Compound
- Aave
- Curve
- Uniswap
- Convex
- And more via DeFiLlama integration

## 🛠️ Technology Stack

- **Node-RED**: Flow-based programming for backend logic
- **DeFiLlama API**: Real-time DeFi yield data source
- **OpenAI API**: AI-powered analysis and recommendations
- **HTML/CSS/JavaScript**: Frontend dashboard
- **Contextual.io**: Hosting platform

## 📋 Prerequisites

- Node-RED installation
- OpenAI API key (for AI features)
- Web browser for dashboard access
- Node.js environment

## 🚀 Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/DeFi-Opportunity-Checker.git
cd DeFi-Opportunity-Checker
```

2. **Import flows to Node-RED**
- Open Node-RED interface
- Navigate to Menu → Import
- Select the flow JSON file
- Click Import

3. **Configure environment variables**
- Set your OpenAI API key in the appropriate nodes
- Configure authentication settings if needed

4. **Deploy the flows**
- Click the Deploy button in Node-RED
- Verify all nodes show green status

## 💻 Usage

### Quick Start
1. Access the dashboard at: `http://your-node-red-instance/dashboard`
2. Login with credentials (default: admin@demo.com / password)
3. View your current portfolio position
4. Review ranked opportunities with risk scores
5. Check AI-powered insights and recommendations

### Bypass Authentication
For testing, access: `http://your-node-red-instance/dashboard?bypass=true`

### API Endpoints

- **GET /dashboard** - Main dashboard interface
- **GET /api/opportunities** - Raw opportunity data
- **POST /api/update-position** - Update portfolio position
- **GET /api/portfolio/{userId}** - Get user portfolio

## 🔧 Configuration

### Customizing Risk Scoring
Edit the "Rank Opportunities" function node to adjust:
- TVL thresholds
- APY risk limits
- Recommendation criteria

### Modifying Data Sources
The "Fetch DeFi Yields" node can be configured to:
- Add additional protocols
- Change minimum TVL filters
- Adjust refresh intervals

### AI Analysis Settings
Configure the OpenAI node with:
- API key
- Model selection (GPT-3.5/GPT-4)
- Temperature and token limits
- Custom prompts for analysis

## 📊 Data Flow

1. **Trigger**: Manual check or scheduled interval
2. **Data Fetch**: Retrieve yields from DeFiLlama API
3. **Parse & Filter**: Process pools meeting criteria (>$10M TVL)
4. **Portfolio Comparison**: Calculate improvements vs current position
5. **Risk Analysis**: Score opportunities based on multiple factors
6. **AI Enhancement**: Generate insights via OpenAI
7. **Dashboard Display**: Present ranked opportunities with recommendations

## 🔒 Security Considerations

- Store API keys securely using Node-RED credentials
- Implement rate limiting for API calls
- Use HTTPS for production deployments
- Regularly rotate authentication tokens
- Validate all user inputs
- Monitor for unusual activity patterns

## 🐛 Troubleshooting

### Common Issues

**API Timeout**: 
- Check network connectivity
- Verify API endpoints are accessible
- Review rate limiting settings

**Missing Opportunities**:
- Ensure minimum TVL filter isn't too restrictive
- Check protocol name matching in filter logic
- Verify API is returning data

**AI Analysis Failures**:
- Confirm OpenAI API key is valid
- Check API quota and billing
- Review error logs for specific issues

## 📈 Performance Optimization

- Implement caching for frequently accessed data
- Use pagination for large result sets
- Optimize database queries if using persistent storage
- Consider CDN for static assets
- Enable compression for API responses

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit changes (`git commit -m 'Add YourFeature'`)
4. Push to branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- DeFiLlama for providing comprehensive DeFi data
- OpenAI for AI capabilities
- Node-RED community for the excellent platform
- Contextual.io for hosting services

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Contact via Discord: [Your Discord]
- Email: support@yourproject.com

## 🗺️ Roadmap

- [ ] Multi-chain support expansion
- [ ] Historical performance tracking
- [ ] Automated position rebalancing
- [ ] Mobile application
- [ ] Advanced portfolio analytics
- [ ] Integration with DeFi wallets
- [ ] Social features for strategy sharing

---

**Disclaimer**: This tool is for informational purposes only. Always do your own research before making investment decisions. DeFi investments carry significant risks.
