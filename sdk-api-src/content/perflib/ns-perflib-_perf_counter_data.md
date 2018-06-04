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

# _PERF_COUNTER_DATA structure


## -description


Contains information about the <b>PERF_COUNTER_DATA</b> block that contains the structure. A <b>PERF_COUNTER_DATA</b> block provides raw performance counter data, and consists of the following items in order: <ol>
<li>A <b>PERF_COUNTER_DATA</b> structure.</li>
<li>Raw performance counter data.</li>
<li>Padding to make the total size of the block a multiple of eight
bytes.</li>
</ol>



## -struct-fields




### -field dwDataSize

The size of the raw performance counter data that follows the <b>PERF_COUNTER_DATA</b> structure in the <b>PERF_COUNTER_DATA</b> block, in bytes.


### -field dwSize

The total size of the <b>PERF_COUNTER_DATA</b> block, which is the sum of the sizes opf the following items:

<ul>
<li>The <b>PERF_COUNTER_DATA</b> structure</li>
<li>The raw performance counter data</li>
<li>The padding that ensures that the size of the  <b>PERF_COUNTER_DATA</b> block is a multiple of 8 bytes</li>
</ul>

## -remarks



The <a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a> function returns a <a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a> block that may contain <b>PERF_COUNTER_DATA</b> blocks directly, or indirectly as part of a <a href="https://msdn.microsoft.com/5EC34ECD-D240-4B44-A52B-C5518918400C">PERF_MULTI_INSTANCES</a> block.




## -see-also




<a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a>
 

 

