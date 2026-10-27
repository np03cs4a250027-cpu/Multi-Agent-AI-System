Multi-Agent AI Sales Proposal Preparation System

An n8n automation workflow designed to streamline the sales proposal preparation process for Vertex Consulting. The system uses multiple specialized AI agents to analyze client requirements, match business needs with approved services, validate pricing and business rules, and generate structured sales proposals for human review.


Core Features

- Multi-Agent Coordination: Uses specialized AI agents for requirement analysis, service matching, pricing validation, proposal writing, and final review.
- Structured Output: Uses JSON to pass consistent information between agents.
- Data Management: Uses n8n Data Tables to store client inquiries, service details, approved pricing, business rules, and proposal guidelines.
- Data Transformation: Uses Edit Fields nodes to clean and prepare relevant data before passing it to each agent, reducing unnecessary token usage.
- Business Rule Validation: Checks approved prices, client budgets, delivery timelines, and service scope.
- Human Review: Requires a salesperson to review and approve the proposal before it is sent to the client.
- Error Handling: Supports troubleshooting for missing information, invalid outputs, and AI model API errors.
- Modular Architecture: Separates responsibilities across agents, making the workflow easier to maintain and extend.


Technology Stack

- Automation Platform: n8n
- AI Model: Google Gemini Chat Model
- Data Format: JSON
- Data Storage: n8n Data Tables
- Data Transformation: Edit Fields nodes
- Execution Environment: Self-hosted n8n using Docker or a local installation
- Human Oversight: Salesperson review and final approval


AI Agent Responsibilities

Requirement Analyst - Analyses the client inquiry and identifies the business problem, primary need, objectives, constraints, and missing information.

Service Matching Agent - Matches the client's needs with suitable services from the approved service catalogue.

Pricing and Rule Checker - Validates pricing, budget compatibility, delivery timelines, and business rules.

Proposal Writer - Generates a professional proposal using verified client, service, and pricing information.

Proposal Reviewer - Checks the proposal for accuracy, completeness, consistency, and compliance before human review.


Data Sources

The system uses structured data to ensure that proposals are based on approved business information.
- Client Inquiries: Client details, business requirements, budgets, preferred timelines, and contact information.
- Service Catalogue: Available services, descriptions, deliverables, delivery times, and starting prices.
- Business Rules: Pricing restrictions, discount policies, budget requirements, timeline requirements, and approval policies.
- Company Information: Vertex Consulting's services, approach, and business objectives.
- Proposal Guidelines: Required proposal sections, writing standards, assumptions, and limitations.


How to Import and Run the Project

Prerequisites

Ensure that you have:
- A working n8n instance running locally or through Docker.
- Google Gemini credentials configured in n8n.
- The required n8n Data Tables populated with project data.
- The exported workflow JSON file.

Import the Workflow
1. Open your n8n dashboard.
2. Create a new workflow or open your existing workflow.
3. Click the three-dot menu in the top-right corner.
4. Select Import from File and upload the exported workflow JSON file.
5. Alternatively, copy the workflow JSON and paste it into the n8n editor if supported by your version.

Configure Credentials and Data
1. Open the Google Gemini Chat Model node.
2. Configure your Gemini API credentials.
3. Check that all Data Table nodes reference the correct tables.
4. Verify that client IDs, service IDs, approved prices, and business rules match the project data.
5. Confirm that each agent receives only the information it needs.

Execute the Workflow
1. Select a client inquiry, such as ABC Retail with client ID C001.
2. Execute the workflow and inspect the Requirement Analyst's structured output.
3. Verify the recommended service and pricing against the approved catalogue and business rules.
4. Review the generated proposal and the Proposal Reviewer's results.
5. Submit the proposal for salesperson review and approval.

Important: The AI-generated proposal is a draft and must not be sent directly to a client without salesperson approval.

Business Rules and Human Oversight

The workflow follows these safeguards:
- Only approved service prices may be used.
- The AI cannot independently approve discounts.
- Significant customization must be flagged for salesperson review.
- Proposed delivery timelines must be consistent with the service catalogue.
- Unsupported services and unverified commitments must not be promised.
- Payment terms must follow the approved business rules.
- Final proposal approval remains the responsibility of a salesperson.

Testing and Validation

Test the workflow using different client inquiries to evaluate:
- Correct identification of business needs.
- Appropriate service recommendations.
- Budget and timeline compatibility.
- Handling of missing or unclear information.
- Compliance with pricing and business rules.
- Accuracy and completeness of the generated proposal.
- Correct operation of human review and approval.

Expected Outcome

The system aims to reduce manual proposal preparation, improve consistency, use approved company information effectively, and help salespeople prepare client-specific proposals more efficiently.

The final output is a structured sales proposal that has passed automated checks and is ready for human review.