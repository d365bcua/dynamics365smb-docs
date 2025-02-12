---
title: Troubleshooting the Shopify and Business Central synchronization
description: Learn what to do if something when wrong during synchronization of data between Shopify and Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---


# Troubleshooting the Shopify and Business Central Synchronization

It's possible to run into situations where you need to troubleshoot issues. This page defines steps to troubleshoot some common scenarios that may arise.

## Logs

If a synchronization task fails, you can activate logging by enabling **Log Enable** toggle in the **Shopify Shop Card**. Manually trigger synchronization task and review logs.

1. Go to the search ![Lightbulb that opens the Tell Me feature.](../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shopify Log Entries**, and choose the related link.
2. Select the related log entry and open the **Shopify Log Entry** window.
3. Review request, status code and description, and response.

Remember to switch off logging to avoid negative performance impact and increase in database size.

From the **Shopify Log Entries** window, you can trigger deletion of all log entries or ones that are older than seven days.

## Data capture

Regardless of the **Log Activated** settings, some responses from Shopify always get logged that you can inspect or download using the **Data Capture List** window.

Choose the **Retrieved Shopify Data** action in one of following pages:

- **Shopify order**
- **Shopify order fulfillments**
- **Shopify order shipping costs**
- **Shopify order transactions**
- **Shopify payouts**
- **Shopify payment transactions**
- **Shopify transactions**

## Reset sync

For optimal performance, the connector imports only customers, products, and orders created or changed since last synchronization. On the **Shopify Shop card**, there are functions available to change date/time of last synchronization or completely reset it. This function ensures that when the sync is run, all data is synced and not just the changes since the last sync.

This function only applies to syncs from Shopify to [!INCLUDE[prod_short](../includes/prod_short.md)] and can be useful if you need to restore deleted data such as products, customers, or deleted orders.

## Update the access token

If [!INCLUDE[prod_short](../includes/prod_short.md)] can't connect to your Shopify account, try resetting the access token.

1. Go to the search ![Lightbulb that opens the Tell Me feature.](../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shopify Shop**, and choose the related link.
2. Select the shop for which you want to get the access token to open the **Shopify Shop Card** page.
3. Choose the **Request Access** action.
4. If prompted, sign in to your Shopify account.

## See Also

[Get Started with the Connector for Shopify](get-started.md)  
