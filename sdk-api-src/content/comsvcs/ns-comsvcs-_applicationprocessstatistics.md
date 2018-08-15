---
UID: NS:comsvcs._ApplicationProcessStatistics
title: "_ApplicationProcessStatistics"
author: windows-sdk-content
description: Represents statistical information about a process hosting COM+ applications.
old-location: cos\applicationprocessstatistics.htm
old-project: cossdk
ms.assetid: 7ce16cef-baa4-491c-89e7-f6283e1a646f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ApplicationProcessStatistics, ApplicationProcessStatistics structure [COM+], _ApplicationProcessStatistics, comsvcs/ApplicationProcessStatistics, cos.applicationprocessstatistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ApplicationProcessStatistics
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - ApplicationProcessStatistics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

