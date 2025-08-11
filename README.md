# Flipkart Product Recommender System

A sophisticated machine learning-powered product recommendation system built with Flask, designed to provide personalized product suggestions based on user behavior and preferences.

## 🚀 Features

- **Intelligent Recommendations**: Advanced algorithms for personalized product suggestions
- **RESTful API**: Clean API endpoints for recommendation services
- **Web Interface**: User-friendly web interface for product discovery
- **Data Processing Pipeline**: Robust data ingestion and preprocessing capabilities
- **Containerized Deployment**: Docker support for easy deployment
- **Kubernetes Ready**: Production-ready Kubernetes configurations
- **Monitoring & Observability**: Integrated Prometheus and Grafana for system monitoring
- **RAG Implementation**: Retrieval Augmented Generation for enhanced recommendations

## 🛠️ Technology Stack

- **Backend**: Python, Flask
- **Machine Learning**: Scikit-learn, Pandas, NumPy
- **Data Processing**: Custom data pipeline with CSV processing
- **Frontend**: HTML, CSS, JavaScript
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **Monitoring**: Prometheus, Grafana
- **Configuration Management**: Python-based config system

## 📁 Project Structure

```
FLIPKART-PRODUCT-RECOMMENDER-SYSTEM/
├── app.py                      # Main Flask application
├── setup.py                    # Package configuration
├── Requirements.txt            # Python dependencies
├── Dockerfile                  # Container configuration
├── flask-deployment.yaml       # Kubernetes deployment
├── FULL DOCUMENTATION.md       # Comprehensive documentation
├── .gitignore                  # Git ignore rules
├── data/                       # Dataset and data files
│   └── flipkart_product_review.csv
├── flipkart/                   # Core recommendation modules
│   ├── __init__.py
│   ├── config.py              # Configuration management
│   ├── data_converter.py      # Data conversion utilities
│   ├── data_ingestion.py      # Data pipeline
│   └── rag_chain.py           # RAG implementation
├── static/                     # Web assets
│   └── style.css              # Stylesheet
├── templates/                  # HTML templates
│   └── index.html             # Main page
├── utils/                      # Utility modules
│   ├── __init__.py
│   ├── exception.py           # Custom exceptions
│   └── logger.py              # Logging configuration
├── grafana/                    # Monitoring configuration
│   └── grafana-deployment.yaml
└── prometheus/                 # Metrics collection
    ├── prometheus-configmap.yaml
    └── prometheus-deployment.yaml
```

## 🚀 Quick Start

### Prerequisites

- Python 3.10+
- Docker (optional)
- Kubernetes cluster (for production deployment)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/rahulsamant37/FLIPKART-PRODUCT-RECOMMENDER-SYSTEM.git
   cd FLIPKART-PRODUCT-RECOMMENDER-SYSTEM
   ```

2. **Install dependencies**
   ```bash
   pip install -r Requirements.txt
   ```

3. **Run the application**
   ```bash
   python app.py
   ```

4. **Access the application**
   - Web Interface: `http://localhost:5000`
   - API Documentation: `http://localhost:5000/api/docs`

### Docker Deployment

1. **Build the container**
   ```bash
   docker build -t flipkart-recommender .
   ```

2. **Run the container**
   ```bash
   docker run -p 5000:5000 flipkart-recommender
   ```

### Kubernetes Deployment

1. **Deploy the application**
   ```bash
   kubectl apply -f flask-deployment.yaml
   ```

2. **Deploy monitoring (optional)**
   ```bash
   kubectl apply -f prometheus/
   kubectl apply -f grafana/
   ```

## 📊 API Endpoints

### Recommendations
- `GET /api/recommendations/<user_id>` - Get personalized recommendations
- `POST /api/recommendations` - Generate recommendations with custom parameters

### Health Check
- `GET /health` - Application health status

## 🔧 Configuration

The application uses a centralized configuration system located in `flipkart/config.py`. Key configurations include:

- Database connections
- Model parameters
- API settings
- Logging levels

## 📈 Monitoring

The system includes comprehensive monitoring with:

- **Prometheus**: Metrics collection and alerting
- **Grafana**: Visualization and dashboards
- **Custom Logging**: Structured logging with configurable levels

## 🧪 Testing

Run tests using:
```bash
python -m pytest tests/
```

## 📚 Documentation

For detailed documentation, refer to:
- `FULL DOCUMENTATION.md` - Comprehensive project documentation
- API documentation available at `/api/docs` when running the application

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat(scope): add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Flipkart for providing the dataset
- Open source community for the amazing tools and libraries
- Contributors and maintainers

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Check the documentation
- Review existing issues and discussions

---

**Built with ❤️ for better product discovery**
```