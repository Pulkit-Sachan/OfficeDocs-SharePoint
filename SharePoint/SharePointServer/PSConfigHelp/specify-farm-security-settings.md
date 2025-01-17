---
title: "Specify farm security settings"
ms.reviewer: 
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 3/1/2018
audience: ITPro
f1.keywords:
- NOCSH
ms.topic: article
ms.prod: sharepoint-server-itpro
ms.localizationpriority: medium
ROBOTS: NOINDEX
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: 01d6f28f-675c-4418-a9ad-fcc8bbfdc58c
description: "Summary: Learn how to use a passphrase in SharePoint Server ."
---

# Specify farm security settings

 **Summary:** Learn how to use a passphrase in SharePoint Server. 
  
Type a passphrase to help to secure farm configuration data, and then select **Next**. 
  
Although a pass phrase is similar to a password, it is usually longer to enhance security. It is used to encrypt credentials of accounts that are registered in SharePoint products, for example, the system account that you provide when you run the SharePoint 2016 Products Configuration Wizard. Ensure that you remember the pass phrase, because you must use it each time you add a server to the farm.
  
Ensure that the passphrase meets the following criteria:
  
- Has at least eight characters
    
- Contains at least three of the following four character groups:
    
  - English uppercase characters (A through Z)
    
  - English lowercase characters (a through z)
    
  - Numerals (0 through 9)
    
  - Nonalphabetic characters (such as !, $, #, %)
    
You can change the passphrase after the farm has been configured by running the **Set-SPPassphrase** cmdlet in Microsoft PowerShell. By default, the new passphrase will be deployed across all servers in the farm. However, if there is a failure in the deployment of the new passphrase, you must manually update the passphrase on the individual server on which the deployment failed. 
  
Run the **Set-SPPassphrase - LocalServerOnly** cmdlet in Microsoft PowerShell to manually update the passphrase. 
  
> [!NOTE]
> When you perform an upgrade, the **Specify Farm Security Settings** page does not appear. 
  

