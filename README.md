# ps-model-pricing

This project provides a structured data repository for tracking AI model pricing details across multiple providers, including OpenAI, Google, Anthropic, and more. The repository includes pricing history for various models, organized for easy analysis and updates.

## Features
- Comprehensive pricing data for AI models, including:
  - Input token pricing (per million tokens)
  - Output token pricing (per million tokens)
  - Effective dates for pricing changes
  - Context window sizes
  - Notes for additional context
- Flat structure for simplicity and ease of use.
- Designed for use in applications that require pricing comparison, historical tracking, or integration into analytics workflows.

## Usage
The data is stored in a single JSON file (`ps-model-pricing.json`), which contains:
- **Providers**: Metadata about each provider (e.g., OpenAI, Google, Anthropic).
- **Models**: Pricing details for each model, with historical entries.

### Example Data Structure
```json
{
  "providers": {
    "openai": {
      "name": "OpenAI",
      "website": "https://openai.com",
      "api_base_url": "https://api.openai.com",
      "models": {
        "gpt-4": {
          "context_window": null,
          "pricing_history": [
            {
              "effective_date": "2024-01-01",
              "input_price_per_million": 30.00,
              "output_price_per_million": 60.00,
              "notes": "Pricing for GPT-4."
            }
          ]
        }
      }
    },
    "google": {
      "name": "Google",
      "website": "https://cloud.google.com",
      "api_base_url": "https://generativelanguage.googleapis.com",
      "models": {
        "gemini-pro": {
          "context_window": null,
          "pricing_history": [
            {
              "effective_date": "2024-01-01",
              "input_price_per_million": 20.00,
              "output_price_per_million": 40.00,
              "notes": "Pricing for Gemini Pro."
            }
          ]
        }
      }
    }
  }
}
```

### How to Contribute
If you have updated pricing data or notice an error in the existing data, feel free to contribute:
1. Fork this repository.
2. Make changes to the JSON file.
3. Submit a pull request with a clear description of your updates.

### MIT License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
