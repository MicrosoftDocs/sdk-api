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

# NLM_CONNECTION_COST enumeration


## -description


The <b>NLM_CONNECTION_COST</b> enumeration specifies a set of cost levels and cost flags supported in Windows 8 Cost APIs.


## -enum-fields




### -field NLM_CONNECTION_COST_UNKNOWN

The cost is unknown.


### -field NLM_CONNECTION_COST_UNRESTRICTED

The connection is unlimited and is considered to be unrestricted of usage charges and capacity constraints.


### -field NLM_CONNECTION_COST_FIXED

The use of this connection is unrestricted up to a specific data transfer limit.


### -field NLM_CONNECTION_COST_VARIABLE

This connection is regulated on a per byte basis.


### -field NLM_CONNECTION_COST_OVERDATALIMIT

The connection is currently in an OverDataLimit state as it has exceeded the carrier specified data transfer limit.


### -field NLM_CONNECTION_COST_CONGESTED

The network is experiencing high traffic load and is congested.


### -field NLM_CONNECTION_COST_ROAMING

The connection is roaming outside the network and  affiliates of the home provider.


### -field NLM_CONNECTION_COST_APPROACHINGDATALIMIT

The connection is approaching the data limit specified by the carrier.


## -remarks



The value returned by the <a href="https://msdn.microsoft.com/66D5FC1A-054C-406E-BEC3-CA62EA09CDF1">INetworkConnectionCost::GetCost</a> method can have multiple bits set with the values specified by this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/66D5FC1A-054C-406E-BEC3-CA62EA09CDF1">INetworkConnectionCost::GetCost</a>
 

 

