---
UID: NS:winperf._PERF_COUNTER_DEFINITION
title: "_PERF_COUNTER_DEFINITION"
author: windows-sdk-content
description: Describes a performance counter.
old-location: perf\perf_counter_definition_str.htm
old-project: perfctrs
ms.assetid: faef043b-81e0-49b0-913f-d691bafd17e6
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*PPERF_COUNTER_DEFINITION, PERF_COUNTER_DEFINITION, PERF_COUNTER_DEFINITION structure [Perf], PERF_DETAIL_ADVANCED, PERF_DETAIL_EXPERT, PERF_DETAIL_NOVICE, PERF_DETAIL_WIZARD, _PERF_COUNTER_DEFINITION, _win32_perf_counter_definition_str, base.perf_counter_definition_str, perf.perf_counter_definition_str, winperf/PERF_COUNTER_DEFINITION"
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
req.typenames: PERF_COUNTER_DEFINITION, *PPERF_COUNTER_DEFINITION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winperf.h
api_name:
 - PERF_COUNTER_DEFINITION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PERF_COUNTER_DEFINITION structure


## -description


Describes a performance counter.


## -struct-fields




### -field ByteLength

Size of this structure, in bytes.


### -field CounterNameTitleIndex

Index of the counter's name in the title database. For details on using the index to retrieve the counter's name, see <a href="https://msdn.microsoft.com/9ddd1672-61cf-41c2-bec0-0d2b775bf970">Retrieving Counter Names and Help Text</a>.

To set this value, providers add the counter's offset value defined in their symbol file to the <b>First Counter</b> registry value. For details, see <a href="https://msdn.microsoft.com/6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4">Adding Counter Names and Descriptions to the Registry</a> and <a href="https://msdn.microsoft.com/0849d9cb-90d1-4b79-810d-b43f69cc9055">Implementing the OpenPerformanceData function</a>.

This value should be zero if the counter is a base counter (<b>CounterType</b> includes the PERF_COUNTER_BASE flag).


### -field CounterNameTitle

Reserved.


### -field CounterHelpTitleIndex

Index to the counter's help text in the title database. For details on using the index to retrieve the counter's help text, see <a href="https://msdn.microsoft.com/9ddd1672-61cf-41c2-bec0-0d2b775bf970">Retrieving Counter Names and Help Text</a>.

To set this value, providers add the counter's offset value defined in their symbol file to the <b>First Help</b> registry value. For details, see <a href="https://msdn.microsoft.com/6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4">Adding Counter Names and Descriptions to the Registry</a> and <a href="https://msdn.microsoft.com/0849d9cb-90d1-4b79-810d-b43f69cc9055">Implementing the OpenPerformanceData function</a>.

This value should be zero if the counter is a base counter (<b>CounterType</b> includes the PERF_COUNTER_BASE flag).


### -field CounterHelpTitle

Reserved.


### -field DefaultScale

Scale factor to use when graphing the counter value. Valid values range from  -7 to 7 (the values correspond to 0.0000001 - 10000000). If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is –1, the scale value is .10; and so on.


### -field DetailLevel

Level of detail for the counter. Consumers use this value to control display complexity. This member can be one of the following values. 



<table>
<tr>
<th>Detail level</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_NOVICE"></a><a id="perf_detail_novice"></a><dl>
<dt><b>PERF_DETAIL_NOVICE</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for all users.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_ADVANCED"></a><a id="perf_detail_advanced"></a><dl>
<dt><b>PERF_DETAIL_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for advanced users.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_EXPERT"></a><a id="perf_detail_expert"></a><dl>
<dt><b>PERF_DETAIL_EXPERT</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for expert users.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_WIZARD"></a><a id="perf_detail_wizard"></a><dl>
<dt><b>PERF_DETAIL_WIZARD</b></dt>
</dl>
</td>
<td width="60%">
The counter data is provided for system designers.

</td>
</tr>
</table>
 


### -field CounterType

Type of counter. For a list of predefined counter types, see the Counter Types section of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84422">Windows Server 2003 Deployment Kit</a>. Consumers use the counter type to determine how to calculate and display the counter value. Providers should limit their choice of counter types to the predefined list. 
					


### -field CounterSize

Counter size, in bytes. 

Currently, only DWORDs (4 bytes) and ULONGLONGs (8 bytes) are used to provide counter values. 


### -field CounterOffset

Offset from the start of the 
<a href="https://msdn.microsoft.com/5cff6142-6d71-46a5-a943-3ec91ebac62b">PERF_COUNTER_BLOCK</a> structure to the first byte of this counter. The location of the <b>PERF_COUNTER_BLOCK</b> structure within the <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> block depends on if the object contains instances. For details, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

Note that multiple counters can use the same raw data and point to the same offset in the <a href="https://msdn.microsoft.com/5cff6142-6d71-46a5-a943-3ec91ebac62b">PERF_COUNTER_BLOCK</a> block.


## -remarks



A <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> structure contains one or more counters. This structure defines each counter and gives the offset to its value.  These structures follow the <b>PERF_OBJECT_TYPE</b> structure in memory. For details, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

Providers should provide their counters in the same order each time their counters are queried. If the counter uses a base counter in its calculation (the counter type includes the <b>PERF_COUNTER_FRACTION</b> flag), the base counter must follow this counter in the list of counters. If the counter type includes the <b>PERF_MULTI_COUNTER</b> flag, the second counter value must follow this counter's value in the <a href="https://msdn.microsoft.com/5cff6142-6d71-46a5-a943-3ec91ebac62b">PERF_COUNTER_BLOCK</a> block.




## -see-also




<a href="https://msdn.microsoft.com/5cff6142-6d71-46a5-a943-3ec91ebac62b">PERF_COUNTER_BLOCK</a>



<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>
 

 

