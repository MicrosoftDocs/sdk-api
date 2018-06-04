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

# INetworkConnectionCostEvents::ConnectionCostChanged


## -description


The <b>ConnectionCostChanged</b> method notifies an application of a network cost change for a connection.


## -parameters




### -param connectionId [in]

A unique ID  that identifies the connection on which the cost change event occurred.


### -param newCost [in]

A DWORD value that represents the new cost of the connection. The lowest 16 bits represent the cost level, and the highest 16 bits represent the flags. Possible values are defined by the <a href="https://msdn.microsoft.com/93541814-A1C3-4C24-BB99-CEE4895F34F8">NLM_CONNECTION_COST</a> enumeration.


## -returns



This method returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/ABFE73E5-CB9E-4077-81D2-DD0FB39F4EC5">INetworkConnectionCostEvents</a>
 

 

