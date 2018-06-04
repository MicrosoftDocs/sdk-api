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

# DsQuerySitesFree function


## -description


The <b>DsQuerySitesFree</b> function frees the memory allocated by the <a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a> function.


## -parameters




### -param rgSiteInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/1920e824-992f-4d69-9b6d-586f58fa2ef7">DS_SITE_COST_INFO</a> structures allocated by a call to <a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/1920e824-992f-4d69-9b6d-586f58fa2ef7">DS_SITE_COST_INFO</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a>
 

 

