---
UID: NE:perflib._PerfCounterDataType
title: "_PerfCounterDataType"
author: windows-driver-content
description: Indicates the content type of a PERF_COUNTER_HEADER block that the PerfQueryCounterData function includes as part of the PERF_DATA_HEADER block that the function produces as output.
old-location: perf\perfcounterdatatype.htm
old-project: PerfCtrs
ms.assetid: E64C73F0-034E-408B-8537-CE6855C01347
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PERF_COUNTERSET, PERF_ERROR_RETURN, PERF_MULTIPLE_COUNTERS, PERF_MULTIPLE_INSTANCES, PERF_SINGLE_COUNTER, PerfCounterDataType, PerfCounterDataType enumeration [Perf], _PerfCounterDataType, perf.perfcounterdatatype, perflib/PERF_COUNTERSET, perflib/PERF_ERROR_RETURN, perflib/PERF_MULTIPLE_COUNTERS, perflib/PERF_MULTIPLE_INSTANCES, perflib/PERF_SINGLE_COUNTER, perflib/PerfCounterDataType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: PerfCounterDataType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Perflib.h
api_name:
-	PerfCounterDataType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PerfCounterDataType enumeration


## -description


Indicates the content type of a <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block that the <a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a> function includes as part of the <a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a> block that the function produces as output.


## -enum-fields




### -field PERF_ERROR_RETURN

An error occurred when the performance counter value was queried.


### -field PERF_SINGLE_COUNTER

The query returned a single counter from a single instance.


### -field PERF_MULTIPLE_COUNTERS

The query returned multiple counters from a single instance.


### -field PERF_MULTIPLE_INSTANCES

The query returned a single counter from each of multiple instances. 


### -field PERF_COUNTERSET

The query returned multiple counters from each of multiple instances.


## -see-also




<a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a>



<a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a>
 

 

