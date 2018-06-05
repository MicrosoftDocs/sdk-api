---
UID: NS:winperf._PERF_COUNTER_BLOCK
title: "_PERF_COUNTER_BLOCK"
author: windows-sdk-content
description: Describes the block of memory that contains the raw performance counter data for an object's counters.
old-location: perf\perf_counter_block_str.htm
old-project: PerfCtrs
ms.assetid: 5cff6142-6d71-46a5-a943-3ec91ebac62b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PPERF_COUNTER_BLOCK, PERF_COUNTER_BLOCK, PERF_COUNTER_BLOCK structure [Perf], _PERF_COUNTER_BLOCK, _win32_perf_counter_block_str, base.perf_counter_block_str, perf.perf_counter_block_str, winperf/PERF_COUNTER_BLOCK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winperf.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PERF_COUNTER_BLOCK, *PPERF_COUNTER_BLOCK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winperf.h
api_name:
-	PERF_COUNTER_BLOCK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PERF_COUNTER_BLOCK structure


## -description



			Describes the block of memory that contains the raw performance counter data for an 
object's counters.
		


## -struct-fields




### -field ByteLength

Size of this structure and the raw counter data that follows, in bytes.


## -remarks



The <b>CounterOffset</b> member of <a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a> provides the offset from the beginning of this structure to the counter value.

The location of the <b>PERF_COUNTER_BLOCK</b> structure within the <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> block depends on if the object contains instances. For details, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

You must ensure that the size of the counter block is aligned to an 8-byte boundary. For example, if the performance object includes two DWORD counters, you must add an additional four bytes to the counter block to make it aligned to an 8-byte boundary.




## -see-also




<a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a>



<a href="https://msdn.microsoft.com/5ea617d3-857d-4e0a-ad10-4d63044fc927">PERF_INSTANCE_DEFINITION</a>



<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>
 

 

