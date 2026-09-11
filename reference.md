# Reference
## Billing
<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getBalanceSummary</a>() -> Talkif.BalanceSummaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/balances
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getBalanceSummary();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">listCharges</a>({ ...params }) -> Talkif.PaginatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Paginated, filterable charge history for an account.
Returns charges with entity context (phone number, flow name, contact name)
from the first associated cost line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.listCharges();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListChargesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getChargeDetail</a>({ ...params }) -> Talkif.ChargeDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Detailed charge view with cost line items breakdown.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getChargeDetail({
    chargeId: "chargeId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetChargeDetailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getBillingCostBreakdown</a>({ ...params }) -> Talkif.AnalyticsCostBreakdownResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get account-level cost breakdown by category with drill-down to calls.

## Query Parameters
- `period`: `today`, `week`, `month`, or `custom` (default: `week`)
- `startDate`: Required when `period=custom`
- `endDate`: Required when `period=custom`

## Response
Returns total costs, breakdown by category (LLM, STT, TTS, telephony),
breakdown by flow, and recent calls with individual cost breakdowns.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getBillingCostBreakdown();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetBillingCostBreakdownRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getBillingCallCostBreakdown</a>({ ...params }) -> Talkif.CallCostBreakdownResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get detailed cost breakdown for a single call with line items.

Returns all cost line items including usage data (tokens, seconds, characters)
and rate information for each cost component.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getBillingCallCostBreakdown({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetBillingCallCostBreakdownRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">listInvoices</a>({ ...params }) -> Talkif.PaginatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/invoices
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.listInvoices();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListInvoicesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getInvoice</a>({ ...params }) -> Talkif.InvoiceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/invoices/{invoiceId}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getInvoice({
    invoiceId: "invoiceId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetInvoiceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getTransactionHistory</a>({ ...params }) -> Talkif.PaginatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/transactions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getTransactionHistory();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetTransactionHistoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getPublicPricing</a>() -> Talkif.PublicPricingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Public endpoint — no authentication required.
Returns telephony rates, phone number pricing, and recording storage pricing.

LLM/STT/TTS pricing is served by `GET /api/v1/models/*` with richer data
(capabilities, languages, use-case filtering).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getPublicPricing();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Calls
<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">makeCall</a>({ ...params }) -> Talkif.MakeCallResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/calls

SECURITY: Verifies account access, phone ownership, provider ownership, flow ownership

Returns:
- 201 Created: Call initiated immediately (capacity available)
- 202 Accepted: Call queued for later processing (at capacity/rate limited)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.makeCall({
    flowId: "550e8400-e29b-41d4-a716-446655440000",
    fromNumber: "+15559876543",
    providerId: "550e8400-e29b-41d4-a716-446655440000",
    toNumber: "+15551234567"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.MakeCallRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getActiveCalls</a>() -> Talkif.CallResponse[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/calls/active
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getActiveCalls();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallHistory</a>() -> Talkif.CallListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/calls/history
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallHistory();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallDetails</a>({ ...params }) -> Talkif.CallResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/calls/:callId
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallDetails({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallDetailsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">analyzeCall</a>({ ...params }) -> Talkif.CallInsights | null</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/calls/:callId/analyze

Generates AI-powered insights from the call transcript:
- Summary (2-3 sentences)
- Sentiment analysis (positive/neutral/negative + confidence)
- Detected intents
- Key topics discussed
- Action items
- Call outcome

This endpoint is always available regardless of account auto-analysis settings.
Can be used to:
- Analyze calls that weren't auto-analyzed
- Re-analyze calls with updated AI model

Requires the call to be in a terminal state (COMPLETED/FAILED/etc.)
and have a transcript available.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.analyzeCall({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AnalyzeCallRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallRecording</a>({ ...params }) -> Talkif.RecordingUrlResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a time-limited presigned URL for recording playback. Fetch the
audio directly from that URL.

Requires the call to belong to the account and to have
`recordingStatus = ready`; recording must be enabled for the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallRecording({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallRecordingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">deleteCallRecording</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/calls/:callId/recording → 204

Charges for actual storage duration before deletion (billing at lifecycle end).
Uses idempotency key to prevent double-charging if racing with retention job.

SECURITY: Verifies account access, call ownership.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.deleteCallRecording({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteCallRecordingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallTranscript</a>({ ...params }) -> Talkif.CallTranscriptResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/calls/:callId/transcript
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallTranscript({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallTranscriptRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Campaigns
<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">listCampaigns</a>({ ...params }) -> core.Page&lt;Talkif.CampaignResponse, Talkif.CampaignListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.campaigns.listCampaigns();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.campaigns.listCampaigns();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListCampaignsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">createCampaign</a>({ ...params }) -> Talkif.CampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.createCampaign({
    flowId: "550e8400-e29b-41d4-a716-446655440000",
    fromPhoneNumber: "+15551234567",
    name: "January Outreach",
    providerId: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">getCampaign</a>({ ...params }) -> Talkif.CampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.getCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">updateCampaign</a>({ ...params }) -> Talkif.CampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.updateCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">deleteCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.deleteCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">cancelCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.cancelCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CancelCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">listCampaignContacts</a>({ ...params }) -> core.Page&lt;Talkif.CampaignContactResponse, Talkif.CampaignContactListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.campaigns.listCampaignContacts({
    campaignId: "campaignId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.campaigns.listCampaignContacts({
    campaignId: "campaignId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListCampaignContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">addCampaignContacts</a>({ ...params }) -> Talkif.AddedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.addCampaignContacts({
    campaignId: "campaignId",
    contactIds: ["contactIds"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AddCampaignContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">removeCampaignContacts</a>({ ...params }) -> Talkif.RemovedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.removeCampaignContacts({
    campaignId: "campaignId",
    campaignContactIds: ["campaignContactIds"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RemoveCampaignContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">bulkAddCampaignContacts</a>({ ...params }) -> Talkif.BulkAddContactsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Bulk add contacts to a campaign using filter criteria.

Instead of passing individual contact IDs, pass filter criteria:
- `tags`: Filter by contact tags (with `tagMode` for ANY/ALL matching)
- `company`: Filter by company name (exact match)
- `search`: Full-text search across name, company, occupation, email

This allows adding thousands of contacts in a single request efficiently.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.bulkAddCampaignContacts({
    campaignId: "campaignId",
    filter: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.BulkAddContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">bulkRemoveCampaignContacts</a>({ ...params }) -> Talkif.BulkRemoveContactsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Bulk remove contacts from a campaign using the same filter criteria as bulk add.

Contacts that already have a call record, or that are sitting in an active
queue slot, are never removed — the response reports `matched` and `removed`
separately so a partial removal is visible rather than silent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.bulkRemoveCampaignContacts({
    campaignId: "campaignId",
    filter: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.BulkRemoveContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">skipCampaignContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark a campaign contact as skipped (e.g., DNC, opt-out, manual skip).
The contact will be excluded from future claiming and calling.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.skipCampaignContact({
    campaignId: "campaignId",
    contactId: "contactId",
    reason: "manual"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SkipContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">pauseCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initiates the draining process for a running campaign:
- Status changes to Draining (stops feeding new contacts to queue)
- Active calls are allowed to complete naturally
- When active_calls_count reaches 0, status transitions to Paused
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.pauseCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PauseCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">restartCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Restarts a campaign for non-called contacts. Resets failed/pending/not-called
contacts back to pending and starts the campaign from Paused/Completed/Cancelled state.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.restartCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RestartCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">resumeCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Resumes a paused campaign, transitioning it back to Running state.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.resumeCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ResumeCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">startCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.startCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.StartCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Analytics
<details><summary><code>client.analytics.<a href="/src/api/resources/analytics/client/Client.ts">getCampaignAnalytics</a>({ ...params }) -> Talkif.CampaignAnalyticsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get deep analytics for a single campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.analytics.getCampaignAnalytics({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCampaignAnalyticsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AnalyticsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.analytics.<a href="/src/api/resources/analytics/client/Client.ts">getFlowStats</a>({ ...params }) -> Talkif.FlowStatsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get statistics for a specific flow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.analytics.getFlowStats({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowStatsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AnalyticsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Contacts
<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">listContacts</a>({ ...params }) -> core.Page&lt;Talkif.Contact, Talkif.ContactListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.contacts.listContacts();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.contacts.listContacts();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createContact({
    name: "Jane Smith",
    primaryPhone: "+15551234567"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">exportContacts</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.exportContacts({
    format: "format"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ExportContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">importContacts</a>({ ...params }) -> Talkif.ImportResult</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.importContacts({
    fileContent: "Sm9obiBEb2UsKzE1NTUxMjM0NTY3",
    format: "vcf"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ImportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">searchByPhone</a>({ ...params }) -> Talkif.ContactSearchResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.searchByPhone({
    phone: "phone"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SearchByPhoneRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">listTags</a>() -> Talkif.TagsListResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.listTags();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContactCalls</a>({ ...params }) -> core.Page&lt;Talkif.CallResponse, Talkif.CallListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.contacts.getContactCalls({
    contactId: "contactId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.contacts.getContactCalls({
    contactId: "contactId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetContactCallsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">restoreContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.restoreContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RestoreContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">addTags</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.addTags({
    contactId: "contactId",
    tags: ["vip", "priority"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AddTagsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">removeTags</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.removeTags({
    contactId: "contactId",
    tags: ["vip"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RemoveTagsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Do Not Call
<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">listDncEntries</a>({ ...params }) -> core.Page&lt;Talkif.DncEntryResponse, Talkif.DncListResponse&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List DNC entries for an account with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.doNotCall.listDncEntries();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.doNotCall.listDncEntries();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListDncEntriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">addDncEntry</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a phone number to the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.addDncEntry({
    phoneNumber: "+15551234567"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateDncEntryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">bulkImportDnc</a>({ ...params }) -> Talkif.BulkDncImportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Bulk import phone numbers to the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.bulkImportDnc({
    phoneNumbers: ["+15551234567", "+15559876543"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.BulkDncImportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">checkDncStatus</a>({ ...params }) -> Talkif.CheckDncResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Check if phone numbers are on the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.checkDncStatus({
    phoneNumbers: ["+15551234567", "+15559876543"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CheckDncRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">removeDncEntry</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a phone number from the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.removeDncEntry({
    phoneNumber: "phoneNumber"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RemoveDncEntryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Errors
<details><summary><code>client.errors.<a href="/src/api/resources/errors/client/Client.ts">errorCatalog</a>() -> Talkif.ErrorCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all API error codes and field validation codes with descriptions, HTTP status codes, and categories. Use this to build error reference documentation or implement client-side error handling.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.errors.errorCatalog();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ErrorsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Flow Functions
<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">listFlowFunctions</a>({ ...params }) -> Talkif.PaginatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-functions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.listFlowFunctions();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListFlowFunctionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">createFlowFunction</a>({ ...params }) -> Talkif.FlowFunctionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flow-functions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.createFlowFunction({
    description: "Create a new customer order",
    name: "create_order",
    request: {
        method: "POST",
        url: "https://api.example.com/orders/{orderId}"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">getFlowFunction</a>({ ...params }) -> Talkif.FlowFunctionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-functions/{id}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.getFlowFunction({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">updateFlowFunction</a>({ ...params }) -> Talkif.FlowFunctionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PUT /api/v1/flow-functions/{id}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.updateFlowFunction({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">deleteFlowFunction</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/flow-functions/{id}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.deleteFlowFunction({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Flow Templates
<details><summary><code>client.flowTemplates.<a href="/src/api/resources/flowTemplates/client/Client.ts">listSystemTemplates</a>({ ...params }) -> Talkif.PaginatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-templates
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowTemplates.listSystemTemplates();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListSystemTemplatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowTemplates.<a href="/src/api/resources/flowTemplates/client/Client.ts">getFlowTemplate</a>({ ...params }) -> Talkif.FlowTemplate</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-templates/:slug

Note: This is a public endpoint that doesn't require auth, but if the user is logged in,
they can also see their account-specific templates
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowTemplates.getFlowTemplate({
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowTemplates.<a href="/src/api/resources/flowTemplates/client/Client.ts">instantiateTemplate</a>({ ...params }) -> Record&lt;string, unknown&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/from-template/:templateSlug
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowTemplates.instantiateTemplate({
    templateSlug: "templateSlug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.InstantiateTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Flows
<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">listFlows</a>() -> Talkif.PaginatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flows

Returns lightweight flow list with connected phones.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.listFlows();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">createFlow</a>({ ...params }) -> Talkif.FlowDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows

Definition is optional — omit to create an empty draft for the builder UI,
or provide it to create a flow with initial content.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.createFlow({
    name: "Appointment Reminder"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">getFlow</a>({ ...params }) -> Talkif.FlowDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flows/:flowId

Returns full flow details including definition, layout, and connected phones.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.getFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">updateFlow</a>({ ...params }) -> Talkif.FlowDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PUT /api/v1/flows/:flowId
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.updateFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">deleteFlow</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/flows/:flowId

Returns 204 No Content on success.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.deleteFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">publishFlow</a>({ ...params }) -> Talkif.PublishFlowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/:flowId/publish
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.publishFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PublishFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">rollbackFlow</a>({ ...params }) -> Talkif.RollbackResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/:flowId/rollback/:version
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.rollbackFlow({
    flowId: "flowId",
    version: "version"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RollbackFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">validateFlow</a>({ ...params }) -> Talkif.ValidationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/:flowId/validate
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.validateFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ValidateFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">getFlowVersion</a>({ ...params }) -> Talkif.FlowVersionDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flows/:flowId/versions/:version
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.getFlowVersion({
    flowId: "flowId",
    version: "version"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowVersionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AI Models
<details><summary><code>client.aiModels.<a href="/src/api/resources/aiModels/client/Client.ts">listProvidersPublic</a>({ ...params }) -> Talkif.FlowProvidersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/models
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aiModels.listProvidersPublic();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListProvidersPublicRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AiModelsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.aiModels.<a href="/src/api/resources/aiModels/client/Client.ts">listTtsVoices</a>({ ...params }) -> Talkif.VoicesDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/models/tts/voices

When any of gender, age, language, accent, or sort are present, routes to
the ElevenLabs /v1/shared-voices endpoint (rich filtering, offset pagination).
Otherwise routes to /v2/voices (simpler, cursor pagination).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aiModels.listTtsVoices();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListTtsVoicesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AiModelsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Phone Numbers
<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">listPhoneNumbers</a>({ ...params }) -> Talkif.PhoneNumberResponse[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.listPhoneNumbers();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListPhoneNumbersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">listAvailableNumbers</a>({ ...params }) -> Talkif.AvailablePhoneNumber[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/twilio/available

Query Parameters:
- `providerId` (required): Provider ID
- `countryCode` (required): ISO country code (e.g., "US", "GB")
- `numberType` (optional): "local", "toll_free", or "mobile" (default: "local")
- `areaCode` (optional): Area code filter (US/Canada only)
- `contains` (optional): Pattern to match (supports wildcards: *, %)
- `inPostalCode` (optional): Filter by postal/ZIP code
- `inRegion` (optional): Filter by state/region
- `inRateCenter` (optional): Filter by rate center
- `inLata` (optional): Filter by LATA
- `inLocality` (optional): Filter by city
- `nearNumber` (optional): Find numbers near this phone number
- `nearLatLong` (optional): Find numbers near lat,long
- `distance` (optional): Radius in miles (default: 25, max: 500)
- `smsEnabled` (optional): Filter SMS-capable numbers
- `mmsEnabled` (optional): Filter MMS-capable numbers
- `voiceEnabled` (optional): Filter voice-capable numbers
- `faxEnabled` (optional): Filter fax-capable numbers
- `beta` (optional): Filter beta numbers
- `excludeAllAddressRequired` (optional): Exclude numbers requiring any address
- `excludeLocalAddressRequired` (optional): Exclude numbers requiring local address
- `excludeForeignAddressRequired` (optional): Exclude numbers requiring foreign address
- `limit` (optional): Max results (default: 20, max: 1000)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.listAvailableNumbers({
    providerId: "providerId",
    countryCode: "countryCode"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListAvailableNumbersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">listAvailableCountries</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/twilio/available-countries
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.listAvailableCountries({
    providerId: "providerId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListAvailableCountriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">getPricing</a>({ ...params }) -> Talkif.PhoneNumberPricing</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/twilio/pricing
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.getPricing({
    providerId: "providerId",
    countryCode: "countryCode"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetPricingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">purchasePhoneNumber</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/phone/numbers/twilio/purchase
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.purchasePhoneNumber({
    phoneNumber: "+15551234567",
    providerId: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PurchasePhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">getPhoneNumber</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.getPhoneNumber({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetPhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">updatePhoneNumber</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PUT /api/v1/phone/numbers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.updatePhoneNumber({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdatePhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">releasePhoneNumber</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/phone/numbers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.releasePhoneNumber({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ReleasePhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">connectFlow</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PATCH /api/v1/phone/numbers/:phoneNumberId/connect-flow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.connectFlow({
    phoneNumberId: "phoneNumberId",
    flowId: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ConnectFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">disconnectFlow</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PATCH /api/v1/phone/numbers/:phoneNumberId/disconnect-flow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.disconnectFlow({
    phoneNumberId: "phoneNumberId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DisconnectFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Phone Providers
<details><summary><code>client.phoneProviders.<a href="/src/api/resources/phoneProviders/client/Client.ts">listPhoneProviders</a>({ ...params }) -> Talkif.PhoneProviderResponse[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/providers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneProviders.listPhoneProviders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListPhoneProvidersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneProvidersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneProviders.<a href="/src/api/resources/phoneProviders/client/Client.ts">getProvider</a>({ ...params }) -> Talkif.PhoneProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/providers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneProviders.getProvider({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetProviderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneProvidersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## PublicCalls
<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">createCall</a>() -> Talkif.CreateWebRtcCallResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls/calls
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.createCall();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">getCallStatus</a>({ ...params }) -> Talkif.PublicCallStatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/public/calls/calls/{callId}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.getCallStatus({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallStatusRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">relayOffer</a>({ ...params }) -> Talkif.WebRtcOfferResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls/calls/{callId}/offer
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.relayOffer({
    callId: "callId",
    sdp: "v=0\r\no=- 0 0 IN IP4 127.0.0.1\r\n..."
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.WebRtcOfferRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">getIceServers</a>() -> Talkif.IceServersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/public/calls/ice-servers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.getIceServers();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">createSession</a>({ ...params }) -> Talkif.CreatePublicSessionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls/session
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.createSession({
    publishableKey: "pk_live_AbCdEf123456"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreatePublicSessionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Schedules
<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">listSchedules</a>({ ...params }) -> core.Page&lt;Talkif.ScheduleResponse, Talkif.ScheduleListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.schedules.listSchedules();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.schedules.listSchedules();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListSchedulesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">createSchedule</a>({ ...params }) -> Talkif.ScheduleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.createSchedule({
    contactId: "550e8400-e29b-41d4-a716-446655440000",
    flowId: "550e8400-e29b-41d4-a716-446655440000",
    frequency: "once",
    fromPhoneNumber: "+15551234567",
    name: "Daily Follow-up Call",
    providerId: "550e8400-e29b-41d4-a716-446655440000",
    scheduleTime: "09:00"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">getSchedule</a>({ ...params }) -> Talkif.ScheduleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.getSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">updateSchedule</a>({ ...params }) -> Talkif.ScheduleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.updateSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">deleteSchedule</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.deleteSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">pauseSchedule</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.pauseSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PauseScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">resumeSchedule</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.resumeSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ResumeScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

