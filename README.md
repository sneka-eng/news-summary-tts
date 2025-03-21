# news-summary-tts
A simple news summarization and text-to-speech application
import json

def get_company_news(company_name):
    data = {
        "Company": company_name,
        "Articles": [
            {
                "Title": f"{company_name}'s New Model Breaks Sales Records",
                "Summary": f"{company_name}’s latest EV sees record sales in Q3...",
                "Sentiment": "Positive",
                "Topics": ["Electric Vehicles", "Stock Market", "Innovation"]
            },
            {
                "Title": f"Regulatory Scrutiny on {company_name}’s Self-Driving Tech",
                "Summary": f"Regulators have raised concerns over {company_name}’s self-driving software...",
                "Sentiment": "Negative",
                "Topics": ["Regulations", "Autonomous Vehicles"]
            }
        ],
        "Comparative Sentiment Score": {
            "Sentiment Distribution": {
                "Positive": 1,
                "Negative": 1,
                "Neutral": 0
            },
            "Coverage Differences": [
                {
                    "Comparison": f"Article 1 highlights {company_name}’s strong sales, while Article 2 discusses regulatory issues.",
                    "Impact": f"The first article boosts confidence in {company_name}’s market growth, while the second raises concerns about future regulatory hurdles."
                },
                {
                    "Comparison": "Article 1 is focused on financial success and innovation, whereas Article 2 is about legal challenges and risks.",
                    "Impact": "Investors may react positively to growth news but stay cautious due to regulatory scrutiny."
                }
            ],
            "Topic Overlap": {
                "Common Topics": ["Electric Vehicles"],
                "Unique Topics in Article 1": ["Stock Market", "Innovation"],
                "Unique Topics in Article 2": ["Regulations", "Autonomous Vehicles"]
            }
        },
        "Final Sentiment Analysis": f"{company_name}’s latest news coverage is mostly positive. Potential stock growth expected.",
        "Audio": "[Play Hindi Speech]"
    }

    return json.dumps(data, indent=4)

# Example usage with user input
company_name = input("Enter the company name: ")
output = get_company_news(company_name)
print(output)
