**Enhanced Toxicity Detection Model with Reinforcement Learning**

This project features a powerful toxicity detection system that leverages an ensemble of machine learning models and a Reinforcement Learning (RL) agent. The system is designed not only to classify text toxicity but also to continuously improve its accuracy by learning from real-time user feedback.
The application is deployed on Hugging Face Spaces with a Gradio interface, making it easily accessible and interactive.

**Key Features**
**Ensemble Model:** Combines the power of XGBoost and Logistic Regression for highly accurate base predictions.
**Adaptive Learning with RL:** A Reinforcement Learning agent actively learns from user corrections, allowing the model to adapt to new and nuanced forms of toxic language.
**Continuous Improvement:** The more feedback the model receives, the more accurate its predictions become over time.
**API Endpoints:** A public-facing API allows for seamless integration with other applications.
**Interactive UI:** The Gradio web interface provides a user-friendly way to test the model and provide feedback.
**Batch Processing:** An API endpoint is available for processing multiple texts in a single request, optimizing performance for large datasets.

**API Endpoints**
The model exposes a set of API endpoints for programmatic access. 
The base URL will be your public Hugging Face Space URL (e.g., **https://[your-space-name].hf.space**).

1) **GET / - Home page:** This is the root of your application. When a user navigates to your base URL (https://...ngrok-free.app), this endpoint serves the initial web page with a simple introduction and a list of available endpoints.

2) **GET /dashboard** - Monitoring dashboard: This endpoint is for the live monitoring dashboard. It serves the HTML page with charts and statistics about the model's performance and the RL agent's learning progress.

3) **POST /api/predict** - Analyze text: This is the core prediction endpoint. A developer sends a single piece of text to this endpoint, and the model returns a full JSON response with the toxicity prediction.

4) **POST /api/feedback** - Submit feedback: This is the endpoint that powers the Reinforcement Learning. Developers can send feedback (correct or incorrect) to this endpoint to help your model continuously improve.

5) **GET /api/stats** - Model statistics: This endpoint provides a real-time snapshot of your model's state in a JSON format. It's useful for monitoring the rl_epsilon and average reward.

6) **POST /api/batch** - Batch analysis: This is an efficient endpoint for processing multiple texts at once. A developer can send a list of comments in a single request and receive an array of predictions.

