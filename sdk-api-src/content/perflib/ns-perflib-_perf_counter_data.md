---
UID: NS:perflib._PERF_COUNTER_DATA
title: "_PERF_COUNTER_DATA"
author: windows-sdk-content
description: Contains information about the PERF_COUNTER_DATA block that contains the structure.
old-location: perf\perf_counter_data.htm
tech.root: perfctrs
ms.assetid: 19D65E98-182E-45CC-946F-F1924CB78029
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: "*PPERF_COUNTER_DATA, PERF_COUNTER_DATA, PERF_COUNTER_DATA structure [Perf], PPERF_COUNTER_DATA, PPERF_COUNTER_DATA structure pointer [Perf], _PERF_COUNTER_DATA, perf.perf_counter_data, perflib/PERF_COUNTER_DATA, perflib/PPERF_COUNTER_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_COUNTER_DATA
product: Windows
targetos: Windows
req.typenames: PERF_COUNTER_DATA, *PPERF_COUNTER_DATA
req.redist: 
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
 

 

