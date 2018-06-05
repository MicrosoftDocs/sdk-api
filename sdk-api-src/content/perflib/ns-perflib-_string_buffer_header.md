---
UID: NS:perflib._STRING_BUFFER_HEADER
title: "_STRING_BUFFER_HEADER"
author: windows-sdk-content
description: Provides information about the PERF_STRING_BUFFER_HEADER block that contains the structure.
old-location: perf\perf_string_buffer_header.htm
old-project: PerfCtrs
ms.assetid: 874A97BA-708E-4001-A7CA-1C3114577D7D
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PPERF_STRING_BUFFER_HEADER, PERF_STRING_BUFFER_HEADER, PERF_STRING_BUFFER_HEADER structure [Perf], PPERF_STRING_BUFFER_HEADER, PPERF_STRING_BUFFER_HEADER structure pointer [Perf], _STRING_BUFFER_HEADER, perf.perf_string_buffer_header, perflib/PERF_STRING_BUFFER_HEADER, perflib/PPERF_STRING_BUFFER_HEADER"
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
req.typenames: PERF_STRING_BUFFER_HEADER, *PPERF_STRING_BUFFER_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Perflib.h
api_name:
-	PERF_STRING_BUFFER_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _STRING_BUFFER_HEADER structure


## -description


Provides information about the <b>PERF_STRING_BUFFER_HEADER</b> block that contains the structure. The <b>PERF_STRING_BUFFER_HEADER</b> block provides the names or help strings for the performance counters in a counter set, amd consists of the following items in order:<ol>
<li>A <b>PERF_STRING_BUFFER_HEADER</b>
structure</li>
<li>A number of <a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a>
structures. The <b>dwCounters</b> member of the <b>PERF_STRING_BUFFER_HEADER</b> structure specifies how many <b>PERF_STRING_COUNTER_HEADER</b>
structures the <b>PERF_STRING_BUFFER_HEADER</b> block contains.</li>
<li>A block of string data.</li>
</ol>



## -struct-fields




### -field dwSize

The total size of the <b>PERF_STRING_BUFFER_HEADER</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_STRING_BUFFER_HEADER</b> structure, all of the <a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a> structures, and the block of string data.


### -field dwCounters

The number of <a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a> structures in the  <b>PERF_STRING_BUFFER_HEADER</b> block.


## -remarks



The <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to
<b>PERF_REG_COUNTER_NAME_STRINGS</b> or <b>PERF_REG_COUNTER_HELP_STRINGS</b> gets a
<b>PERF_STRING_BUFFER_HEADER</b> block.




## -see-also




<a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a>



<a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a>
 

 

