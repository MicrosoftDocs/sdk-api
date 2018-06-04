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

# CFrameworkQuery::GetQuery


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetQuery</b> method retrieves the actual WQL command associated with the <a href="https://msdn.microsoft.com/60a7d83c-cfea-41fa-8d97-321127d33c43">CFrameworkQuery</a> object.


## -parameters






## -returns



Returns the WQL command if the operation was successful and <b>NULL</b> otherwise.




## -remarks



If <b>GetQuery</b> is called within <a href="https://msdn.microsoft.com/c8e2633a-cbea-422c-9598-1b1b1104bbc2">Provider::GetObject</a>, the WQL command line does not contain a <a href="https://msdn.microsoft.com/9c1a164e-4728-4fbe-8a49-b571005a46ec">WHERE</a> clause.



