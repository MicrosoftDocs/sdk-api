---
UID: NS:perflib._PERF_MULTI_COUNTERS
title: "_PERF_MULTI_COUNTERS"
author: windows-sdk-content
description: Provides information about the PERF_MULTI_COUNTERS block that contains the structure.
old-location: perf\perf_multi_counters.htm
old-project: PerfCtrs
ms.assetid: 4F490C3C-F587-4E7B-B316-162EDA76EC30
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PPERF_MULTI_COUNTERS, PERF_MULTI_COUNTERS, PERF_MULTI_COUNTERS structure [Perf], PPERF_MULTI_COUNTERS, PPERF_MULTI_COUNTERS structure pointer [Perf], _PERF_MULTI_COUNTERS, perf.perf_multi_counters, perflib/PERF_MULTI_COUNTERS, perflib/PPERF_MULTI_COUNTERS"
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
tech.root: 
req.typenames: PERF_MULTI_COUNTERS, *PPERF_MULTI_COUNTERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_MULTI_COUNTERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PERF_MULTI_COUNTERS structure


## -description


Provides information about the <b>PERF_MULTI_COUNTERS</b> block that contains the structure. A <b>PERF_MULTI_COUNTERS</b> block indicates the performance counters for which results are provided as part of the <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block in multiple-counter query. The <b>PERF_MULTI_COUNTERS</b> block consists of a <b>PERF_MULTI_COUNTERS</b> structure
followed by a sequence of <b>DWORD</b> values that specify performance counter identifiers.


## -struct-fields




### -field dwSize

The total size of the <b>PERF_MULTI_COUNTERS</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_MULTI_COUNTERS</b> structure and all of the performance counter identifiers.


### -field dwCounters

The number of performance counter identifiers that the <b>PERF_MULTI_COUNTERS</b> block contains.


## -remarks



The <a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a> function gets a <a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a> block that may
contain a <b>PERF_MULTI_COUNTERS</b> block within the <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block.




## -see-also




<a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a>



<a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a>



<a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a>
 

 

