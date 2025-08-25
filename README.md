# LinkedIn News Article Comment Generator - n8n Workflow

This n8n workflow automates LinkedIn content creation including news generation, article creation, and comment generation for AI and ML topics.

## Setup Instructions

Before importing this workflow, you'll need to configure the following credentials in your n8n instance:

### Required API Credentials

1. **Anthropic API** (`ANTHROPIC_API_CREDENTIAL_ID`)
   - Used for Claude 4 Sonnet models
   - Get your API key from: https://console.anthropic.com/

2. **OpenAI API** (`OPENAI_API_CREDENTIAL_ID`)
   - Used for GPT models and image generation
   - Get your API key from: https://platform.openai.com/api-keys

3. **Google APIs** (OAuth2 required):
   - **Google Docs** (`GOOGLE_DOCS_OAUTH2_CREDENTIAL_ID`)
   - **Google Drive** (`GOOGLE_DRIVE_OAUTH2_CREDENTIAL_ID`)
   - **Google Sheets** (`GOOGLE_SHEETS_OAUTH2_CREDENTIAL_ID`)
   - Set up OAuth2 at: https://console.cloud.google.com/

4. **Tavily API** (`TAVILY_API_CREDENTIAL_ID`)
   - Used for web research
   - Get your API key from: https://tavily.com/

5. **SerpAPI** (`SERPAPI_CREDENTIAL_ID`)
   - Used for search functionality
   - Get your API key from: https://serpapi.com/

6. **Perplexity API** (`PERPLEXITY_API_CREDENTIAL_ID`)
   - Used for AI-powered research
   - Get your API key from: https://www.perplexity.ai/

### Webhook Configuration

The workflow uses three webhook triggers that will need to be reconfigured:

1. `WEBHOOK_ID_CHAT_TRIGGER` - Main chat trigger
2. `WEBHOOK_ID_ARTICLE_GENERATOR` - Article generation trigger
3. `WEBHOOK_ID_COMMENT_GENERATOR` - Comment generation trigger

## Workflow Components

### 1. LinkedIn Latest News Generator
Generates 10 current news items in AI and ML, ranked by relevance.

### 2. LinkedIn Article Generator
Creates comprehensive articles with accompanying images for social media posts.

### 3. LinkedIn Comment Generator
Generates contextual comments for posts created by other LinkedIn members.

## Features

- **Multi-AI Integration**: Uses Claude, GPT, and Perplexity for diverse content generation
- **Research Capabilities**: Integrates with Tavily, SerpAPI, and Perplexity for current information
- **Google Workspace Integration**: Automatically saves content to Google Docs and Sheets
- **Image Generation**: Creates relevant images using OpenAI's DALL-E
- **Cloud Storage**: Uploads generated images to Google Drive

## Usage

1. Import the workflow into your n8n instance
2. Configure all required credentials with your API keys
3. Update webhook URLs as needed
4. Test each component individually before running the full workflow

## Notes

- All sensitive credential IDs have been replaced with placeholder names for security
- You'll need to replace these placeholders with your actual credential IDs in n8n
- Ensure all API quotas and limits are appropriate for your usage
- Test in a development environment before using in production
