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

# _PERF_DATA_HEADER structure


## -description


Provides information about the <b>PERF_DATA_HEADER</b> block that contains the structure. A <b>PERF_DATA_HEADER</b> block corresponds to one query specification in a query, and consists of a <b>PERF_DATA_HEADER</b>
structure followed by a sequence of <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> blocks.


## -struct-fields




### -field dwTotalSize

The sum of the size of the <b>PERF_DATA_HEADER</b> structure and the sizes of all of the <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> blocks in the <b>PERF_DATA_HEADER</b> block. 


### -field dwNumCounters

The number of <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> blocks that the <b>PERF_DATA_HEADER</b> block contains.


### -field PerfTimeStamp

The timestamp from a high-resolution clock.


### -field PerfTime100NSec

The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).


### -field PerfFreq

The frequency of a high-resolution clock.


### -field SystemTime

The time at which data is collected by the provider.


## -remarks



The ordering of the <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> blocks is based on the <b>Index</b> member of
the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> blocks that the <a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a> function gets. Each
<b>PERF_COUNTER_HEADER</b> block is 8-byte aligned, so the value of the <b>dwTotalSize</b> is  a multiple
of 8 bytes.



The timestamp information in the <b>PERF_DATA_HEADER</b> structure is required when
you compute the display values of certain performance counters.





## -see-also




<a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a>



<a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a>
 

 

