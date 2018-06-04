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

# _ApplicationProcessStatistics structure


## -description


Represents statistical information about a process hosting COM+ applications.


## -struct-fields




### -field NumCallsOutstanding

The number of calls currently outstanding in tracked components in the process.


### -field NumTrackedComponents

The number of distinct tracked components instantiated in the process.


### -field NumComponentInstances

The number of component instances in the process.


### -field AvgCallsPerSecond

A rolling average of the number of calls this process is servicing per second.


### -field Reserved1

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved2

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved3

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved4

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

