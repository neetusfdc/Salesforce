# Salesforce

Salesforce DX source for an Opportunity browsing experience.

## Included metadata

- `OpportunityController` Apex class exposing a cacheable, sharing-aware
  Opportunity query to Lightning via `@AuraEnabled`, with name search, stage
  filtering, allowlisted sorting, and server-side pagination
- `OpportunityControllerTest` covering search, stage filtering, sorting,
  pagination, and stage picklist options
- `opportunityList` LWC rendering Opportunity Name, Account, Stage, Amount, and
  Close Date in a `lightning-datatable`

## Deploy and use

1. Authenticate with a Salesforce org using Salesforce CLI.
2. Deploy the source with `sf project deploy start --source-dir force-app`.
3. Run the Apex tests with `sf apex run test --tests OpportunityControllerTest --result-format human --wait 10`.
4. Add **Opportunity List** to a Lightning page in Lightning App Builder.
