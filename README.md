# PropChain Backend

> 🏠 **Decentralized Real Estate Infrastructure** | Backend API for blockchain-powered property transactions

PropChain Backend is a production-grade server-side infrastructure that enables the tokenization and trading of real estate assets through blockchain technology. Our API provides the core services needed to build decentralized real estate platforms, including smart contract integration, secure transaction processing, and comprehensive property management capabilities.

Built with enterprise-grade technologies, this backend serves as the foundation for Web3 real estate applications, enabling developers to create platforms where physical properties can be represented as digital assets and traded seamlessly using cryptocurrency.

## 🚀 Features

### Core Capabilities
- **🏠 Asset Tokenization**: Transform physical real estate properties into tradable NFTs with legal compliance
- **💰 Crypto Transaction Processing**: Secure, multi-chain cryptocurrency payment processing
- **🔗 Smart Contract Integration**: Pre-built contracts for property ownership, transfers, and escrow
- **📊 Property Management APIs**: Complete CRUD operations for real estate listings and metadata
- **🔐 Web3 Authentication**: Wallet-based user authentication with role-based access control
- **💾 Enterprise Data Storage**: Scalable PostgreSQL database with migration support

### Advanced Features
- **🌐 Multi-Chain Support**: Ethereum, Polygon, and BSC network compatibility
- **📈 Real-Time Analytics**: Property valuation trends and market insights
- **🔍 Search & Discovery**: Advanced filtering and geospatial property search
- **📱 Mobile-Ready API**: RESTful endpoints optimized for mobile applications
- **🛡️ Security First**: Built-in rate limiting, input validation, and audit logging

## 👥 Target Audience

This backend is designed for:
- **Real Estate Tech Companies** building blockchain-based property platforms
- **Property Investment Firms** seeking fractional ownership solutions
- **Blockchain Developers** creating DeFi real estate applications
- **Real Estate Agencies** modernizing their transaction infrastructure
- **FinTech Startups** integrating real estate into their crypto ecosystems

## 🛠️ Quick Start

### Prerequisites
Ensure you have the following installed:
- **Node.js** v18+ (LTS recommended)
- **npm** or **yarn** package manager
- **PostgreSQL** v14+ 
- **Rust** toolchain (for smart contract compilation)
- **Git** version control

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/MettaChain/PropChain-BackEnd.git
cd PropChain-BackEnd

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env
# Edit .env with your configuration

# 4. Initialize database
createdb propchain
npm run migrate

# 5. Start development server
npm run dev
```

The API will be available at `http://localhost:3000` with interactive Swagger docs at `http://localhost:3000/api`.

## 🚀 Deployment & Operations

### Development Environment
```bash
npm run dev          # Start development server with hot reload
npm run start:dev    # Start with debug logging
npm run test:watch   # Run tests in watch mode
```

### Production Deployment
```bash
npm run build        # Compile TypeScript to JavaScript
npm start            # Start production server
npm run health       # Health check endpoint
```

### Testing Suite
```bash
npm test             # Run unit tests
npm run test:integration    # Run integration tests
npm run test:e2e           # Run end-to-end tests
npm run test:coverage      # Generate coverage report
npm run test:contracts     # Test smart contracts
```

### Smart Contract Management
```bash
npm run compile:contracts  # Compile Rust/Solidity contracts
npm run deploy:testnet     # Deploy to testnet
npm run deploy:mainnet     # Deploy to mainnet
npm run verify:contracts  # Verify on Etherscan
```

## 🌐 Network Configuration

### Supported Blockchains
- **Ethereum** (Mainnet, Sepolia Testnet)
- **Polygon** (Mainnet, Mumbai Testnet) 
- **Binance Smart Chain** (Mainnet, Testnet)
- **Local Development** (Hardhat Network)

### Environment Configuration
```env
# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/propchain

# Blockchain
BLOCKCHAIN_NETWORK=sepolia
RPC_URL=https://sepolia.infura.io/v3/YOUR_PROJECT_ID
PRIVATE_KEY=your_private_key_here

# Security
JWT_SECRET=your_jwt_secret_key
API_KEY=your_api_key

# Services
REDIS_URL=redis://localhost:6379
WEB3_STORAGE_TOKEN=your_web3_storage_token
```

## 📚 Documentation & Resources

### API Documentation
- **[📖 API Reference](./docs/api.md)** - Complete REST API documentation with examples
- **[🔗 Smart Contracts](./docs/contracts.md)** - Contract interfaces and integration guides
- **[🚀 Deployment Guide](./docs/deployment.md)** - Production deployment best practices
- **[🏗️ Architecture](./docs/architecture.md)** - System design and technical architecture

### Repository Structure
```
PropChain-BackEnd/
├── 📁 src/
│   ├── 📁 controllers/     # API route handlers and request processing
│   ├── 📁 services/        # Business logic and external service integrations
│   ├── 📁 models/          # Database models and schemas (Prisma)
│   ├── 📁 middleware/      # Authentication, validation, and error handling
│   ├── 📁 utils/           # Helper functions and utilities
│   ├── 📁 config/          # Configuration management
│   └── 📁 types/           # TypeScript type definitions
├── 📁 contracts/           # Smart contracts (Rust/Solidity)
├── 📁 migrations/          # Database migration files
├── 📁 tests/              # Unit, integration, and E2E tests
├── 📁 docs/               # Comprehensive documentation
├── 📁 scripts/            # Build, deployment, and utility scripts
├── 📁 .github/            # CI/CD workflows and issue templates
└── 📁 docker/             # Docker configuration files
```

### Contributing
- **[🤝 Contributing Guide](./CONTRIBUTING.md)** - How to contribute effectively
- **[📋 Code of Conduct](./CODE_OF_CONDUCT.md)** - Community guidelines and standards
- **[🐛 Issue Templates](./.github/ISSUE_TEMPLATE/)** - Standardized issue reporting
- **[💡 Feature Requests](./.github/ISSUE_TEMPLATE/feature_request.md)** - Feature proposal template

### Additional Resources
- **[🌐 Frontend Application](https://github.com/MettaChain/PropChain-FrontEnd)** - Client-side React/Next.js application
- **[🔒 Security Audits](./audits/)** - Third-party security audit reports
- **[📊 Performance Metrics](./docs/performance.md)** - Benchmarks and optimization guides
- **[🎓 Tutorials](./docs/tutorials/)** - Step-by-step integration tutorials

## 🛠️ Technology Stack

### Backend Infrastructure
- **🚀 Framework**: NestJS (Node.js/TypeScript) - Enterprise-grade application framework
- **🗄️ Database**: PostgreSQL v14+ with Prisma ORM - Type-safe database access
- **🔍 Caching**: Redis - High-performance caching and session storage
- **📊 Message Queue**: Bull Queue - Background job processing

### Blockchain & Web3
- **⛓️ Networks**: Ethereum, Polygon, BSC - Multi-chain compatibility
- **🔗 Web3 Library**: ethers.js - Modern Ethereum JavaScript library
- **📝 Smart Contracts**: Solidity (EVM) + Rust (Solana) - Cross-platform contracts
- **🔐 Wallet Integration**: MetaMask, WalletConnect - Multi-wallet support

### Development & Operations
- **🧪 Testing**: Jest + Supertest - Comprehensive testing suite
- **📝 API Docs**: Swagger/OpenAPI 3.0 - Interactive API documentation
- **🐳 Containerization**: Docker + Docker Compose - Consistent deployments
- **🔄 CI/CD**: GitHub Actions - Automated testing and deployment
- **📊 Monitoring**: Prometheus + Grafana - Performance metrics and alerts

### Security & Compliance
- **🔐 Authentication**: JWT + Web3 signatures - Secure user verification
- **🛡️ Security**: Helmet, CORS, Rate Limiting - Production-grade security
- **📋 Validation**: class-validator - Request data validation
- **🔍 Auditing**: Comprehensive audit logging for compliance

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for complete details.

## 🤝 Support & Community

### Get Help
- **🐛 Report Issues**: [GitHub Issues](https://github.com/MettaChain/PropChain-BackEnd/issues)
- **📧 Email Support**: support@propchain.io
- **📖 Documentation**: [docs.propchain.io](https://docs.propchain.io)

### Contributing
We welcome contributions! Please read our [Contributing Guide](./CONTRIBUTING.md) to get started. 

**Quick contribution steps:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

<div align="center">

**⭐ Star this repository if it helped you!**

Made with ❤️ by the PropChain Team

</div>
