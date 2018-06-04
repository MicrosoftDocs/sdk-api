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

# GROUP_FAILURE_INFO structure


## -description


Represents information about the <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">Failover</a> attempts for a group failure.


## -struct-fields




### -field dwFailoverAttemptsRemaining

The number of remaining failover attempts that can be made on the group during the current <a href="https://msdn.microsoft.com/5277a4a7-2866-4c16-8ad0-ea3a33714583">FailoverPeriod</a>  time interval.


### -field dwFailoverPeriodRemaining

The amount of time remaining for the <a href="https://msdn.microsoft.com/5277a4a7-2866-4c16-8ad0-ea3a33714583">FailoverPeriod</a>, in hours.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

