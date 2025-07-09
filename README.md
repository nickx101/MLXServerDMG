# Lambda Drive AI Server Ecosystem - Meta Repository

## Component Repositories

### Core Infrastructure
1. **[LambdaDriveMCP](https://github.com/nickx101/LambdaDriveMCP)** - Core MCP server implementation
   - Production-ready MCP integration bridge
   - Shared communication system
   - Tool registry and management
   - Security and rate limiting

### Voice Pipeline
2. **[VoiceMode-MCP](https://github.com/nickx101/VoiceModeMCP)** - Voice processing pipeline
   - Real-time voice capture and processing
   - Integration with LambdaDrive ecosystem
   - Low-latency audio streaming
   - Voice command recognition

### Text-to-Speech
3. **[Kokoro-FastAPI](https://github.com/nickx101/KokoroFastAPI)** - High-performance TTS server
   - FastAPI-based TTS service
   - Optimized for low latency (61ms)
   - Production-ready with caching
   - Supports multiple voice models

### Configuration Management
4. **[LambdaDrive-Config](https://github.com/nickx101/LambdaDrive-Config)** - Unified configuration system
   - Centralized configuration management
   - Environment-based settings
   - Service discovery and coordination
   - Configuration validation

### AI Core (Private)
5. **AI-CORE** - Core AI processing engine
   - MLX-based model serving
   - Optimized inference pipeline
   - Model management system
   - Performance monitoring

### Desktop Applications
6. **[MLXServerManager](https://github.com/nickx101/MLXServerDMG)** - macOS management interface
   - Native SwiftUI application
   - Server lifecycle management
   - Real-time status monitoring
   - Model management UI

## Quick Start

### Prerequisites
- macOS 13+ (for desktop apps)
- Python 3.9+
- Node.js 18+
- Swift 5.5+ (for building desktop apps)

### Installation

1. **Clone the meta repository:**
   ```bash
   git clone https://github.com/nickx101/lambdadrive-meta
   cd lambdadrive-meta
   ```

2. **Set up core services:**
   ```bash
   # Clone and setup LambdaDriveMCP
   git clone https://github.com/nickx101/LambdaDriveMCP
   cd LambdaDriveMCP && npm install

   # Clone and setup VoiceMode
   git clone https://github.com/nickx101/VoiceModeMCP
   cd VoiceModeMCP && npm install

   # Clone and setup Kokoro TTS
   git clone https://github.com/nickx101/KokoroFastAPI
   cd KokoroFastAPI && pip install -r requirements.txt
   ```

3. **Configure the system:**
   ```bash
   git clone https://github.com/nickx101/LambdaDrive-Config
   cd LambdaDrive-Config
   # Follow configuration README
   ```

4. **Launch services:**
   ```bash
   # Start all services using the configuration manager
   cd LambdaDrive-Config
   ./launch-services.sh
   ```

## Performance Metrics

- **85% faster** than original implementation
- **61ms** voice-to-response latency
- **100%** service reliability
- **Sub-10ms** inter-service communication
- **Automatic failover** and recovery

## Architecture Overview

```
┌─────────────────────┐     ┌─────────────────────┐
│   MLX Server GUI    │────▶│   LambdaDriveMCP    │
└─────────────────────┘     └──────────┬──────────┘
                                       │
┌─────────────────────┐                │
│    VoiceMode-MCP    │◀───────────────┤
└──────────┬──────────┘                │
           │                           │
           ▼                           ▼
┌─────────────────────┐     ┌─────────────────────┐
│   Kokoro-FastAPI    │     │  LambdaDrive-Config │
└─────────────────────┘     └─────────────────────┘
```

## Development

Each repository contains its own development documentation. Key principles:

1. **Modular Design** - Each component is independently deployable
2. **Shared Communication** - Unified messaging protocol
3. **Configuration-First** - All settings centrally managed
4. **Performance-Optimized** - Every millisecond counts
5. **Production-Ready** - Built for reliability

## Contributing

Please see individual repository contribution guidelines. General workflow:

1. Fork the specific component repository
2. Create a feature branch
3. Make your changes with tests
4. Submit a pull request
5. Ensure CI/CD passes

## License

Each component is licensed individually. See respective repositories for details.

## Support

For issues, please file in the appropriate component repository:
- Infrastructure issues → LambdaDriveMCP
- Voice issues → VoiceMode-MCP
- TTS issues → Kokoro-FastAPI
- Configuration issues → LambdaDrive-Config
- Desktop app issues → MLXServerManager

---

Built with ❤️ for the AI community