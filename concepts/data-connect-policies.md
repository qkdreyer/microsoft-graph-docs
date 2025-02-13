---
title: "Microsoft Graph Data Connect policies and licensing"
description: "Describes what policies are supported and how to assign ISV access SKUs to organizations."
author: "fercobo-msft"
ms.localizationpriority: high
ms.prod: "data-connect"
---

# Microsoft Graph Data Connect policies and billing

Microsoft Graph Data Connect uses [Azure managed applications](/azure/managed-applications/overview) to allow you to create and deploy your solutions in your Azure environment. Managed applications allow you to support certain Azure policies, giving customers greater confidence and comfortability when using your applications.

## Policies

The following Azure policies are supported for an Azure managed application built using Microsoft 365 data:

- [Azure Storage and ADLS Gen 2 required policy](/azure/storage/common/policy-reference)
- [ADLS Gen1 required policy](/azure/data-lake-store/policy-reference)

> [!NOTE]
> Azure Data Lake Store Gen 1 and Gen 2 use different policies because ADLS Gen 2 implements Azure Storage.

When you select any of the policies during Azure marketplace publishing, the policy compliance status will be checked and enforced for all installations of your application. All selected policies that are compliant will be shown to the data approvers as part of the data request. Any policy compliance violation would cause the pipeline run to fail and stop the data extraction.

## Billing for Microsoft Graph Data Connect

The bill will be associated with the Azure Subscription of the Azure Data Factory you are using. The price in this new billing model is based on the number of Microsoft Graph objects you are accessing.

While this new billing capability is in preview, the rate is $0.375 for 1,000 Microsoft Graph objects. For example, if you access 10,000 total objects, you will receive an Azure bill for $3.75. At the end of the preview period, the rate will be $0.75 per 1,000 Microsoft Graph objects.

Directory objects that will not be charged are:

- BasicDataSet_v0.User
- BasicDataSet_v0.MailboxSettings
- BasicDataSet_v0.Manager
- BasicDataSet_v0.DirectReport

## See also

- [Azure Storage policies](/azure/storage/common/policy-reference)
- [Microsoft Graph Data Connect billing](https://azure.microsoft.com/pricing/details/graph-data-connect/)
- [Azure managed applications](/azure/managed-applications/overview)
- [User selection and filtering](data-connect-filtering.md)
- [Data Connect frequently asked questions](data-connect-faq.md)
