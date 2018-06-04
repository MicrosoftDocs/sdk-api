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

# NLM_USAGE_DATA structure


## -description


The<b>NLM_USAGE_DATA</b> structure stores information that indicates the data usage  of a plan.


## -struct-fields




### -field UsageInMegabytes

The data usage of a plan, represented in megabytes.


### -field LastSyncTime

The timestamp of last time synced with carriers about the data usage stored in this structure.


## -remarks



If usage is not supplied, <b>UsageInMegabytes</b> is set to <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> (0xFFFFFFFF), and <b>LastSyncTime</b> is set to 0.




## -see-also




<a href="https://msdn.microsoft.com/82B4FF65-5D45-4D79-8F11-EA4CF4760EE2">INetworkCostManager::GetDataPlanStatus</a>



<a href="https://msdn.microsoft.com/49774150-FD7E-4541-95DF-C848247A6A9C">NLM_DATAPLAN_STATUS</a>
 

 

