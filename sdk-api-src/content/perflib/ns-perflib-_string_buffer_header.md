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
 

 

