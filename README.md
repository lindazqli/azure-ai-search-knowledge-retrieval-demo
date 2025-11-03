# Azure AI Search – Foundry Knowledge Demo

Production-ready Next.js app demonstrating advanced RAG with Azure AI Search Knowledge Bases and Azure AI Foundry Agent Service.

## Deploy to Cloud

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ffarzad528%2Fazure-ai-search-knowledge-retrieval-demo%2Fmain%2Finfra%2Fmain.json)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Ffarzad528%2Fazure-ai-search-knowledge-retrieval-demo)

## Quick Start (Local)

```bash
git clone https://github.com/farzad528/azure-ai-search-knowledge-retrieval-demo.git
cd azure-ai-search-knowledge-retrieval-demo
npm install
cp .env.example .env.local
```

Edit `.env.local` with your Azure credentials:

```bash
# Required: Azure AI Search + Azure OpenAI
AZURE_SEARCH_ENDPOINT=https://<your-search>.search.windows.net
AZURE_SEARCH_API_KEY=<admin-or-query-key>
AZURE_SEARCH_API_VERSION=2025-11-01-preview
NEXT_PUBLIC_AZURE_OPENAI_ENDPOINT=https://<your-openai>.openai.azure.com
AZURE_OPENAI_API_KEY=<openai-key>

# Optional: Azure AI Foundry Agent Service
FOUNDRY_PROJECT_ENDPOINT=https://<resource>.services.ai.azure.com/api/projects/<project>
FOUNDRY_API_VERSION=2025-05-01
AZURE_AUTH_METHOD=service-principal
AZURE_TENANT_ID=<tenant-id>
AZURE_CLIENT_ID=<app-id>
AZURE_CLIENT_SECRET=<secret>
```

Start the app:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

## Recorded Demo

<!-- Video placeholder - coming soon -->
_Video walkthrough coming soon_

## Application Routes

### 1. Knowledge (`/knowledge`)
View all knowledge bases from your Azure AI Search resource. In **Admin Mode**, create and update knowledge bases with diverse sources (Blob Storage, Search Index, Web, SharePoint, OneLake).

**Use when:** You need to manage knowledge bases and configure data sources.

### 2. Playground (`/playground`)
Interactive playground for querying knowledge bases with full control over runtime settings (retrieval reasoning effort, output mode, source-specific parameters, reranker threshold).

**Use when:** You want advanced RAG experimentation, testing different retrieval strategies, or adjusting query behavior over your data.

### 3. Agents (`/agents`)
Explore Azure AI Foundry Agent Service integration with Knowledge Bases.

**Use when:** You need a production-ready managed agent service with built-in orchestration for diverse knowledge sources and multi-turn conversations.

## Contributing

PRs welcome. Keep changes small and typed. Run `npm run build` before submitting.

## License

MIT – see `LICENSE`.

## Resources

- [Azure AI Search Documentation](https://learn.microsoft.com/azure/search/)
- [Azure AI Foundry Documentation](https://learn.microsoft.com/azure/ai-foundry/)
