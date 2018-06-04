---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICOMAdminCatalog::RefreshComponents


## -description


Updates component registration information from the registry.

You generally should not use <b>RefreshComponents</b>. The recommended way to update components in COM+ applications is to remove and reinstall the components using <a href="https://msdn.microsoft.com/63af9aa4-a1f0-4277-bd36-8b4c64227b3f">ICOMAdminCatalog::InstallComponent</a> so that complete registration information is updated in the registry database.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <b>RefreshComponents</b> method is called from within the Microsoft Visual Basic 6.0 development environment when you use the <b>Auto-refresh</b> or <b>Refresh all</b> components now features from the <b>Component Services</b> submenu of the <b>Add-Ins</b> menu.

To find mismatches, <b>RefreshComponents</b> compares CLSIDs and ProgIDs between the COM+ class registration database (RegDB) and the registry. This method updates components only when there is both a mismatch between CLSIDs and a match between corresponding ProgIDs.

Only CLSID information is updated to RegDB. No interface or method information is updated. Components that are refreshed using <b>RefreshComponents</b> cannot be configured or secured at the interface or method levels within COM+ applications.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

