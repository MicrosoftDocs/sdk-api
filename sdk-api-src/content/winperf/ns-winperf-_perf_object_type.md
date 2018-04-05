---
UID: NS:winperf._PERF_OBJECT_TYPE
title: "_PERF_OBJECT_TYPE"
author: windows-driver-content
description: Describes object-specific performance information, for example, the number of instances of the object and the number of counters that the object defines.
old-location: perf\perf_object_type_str.htm
old-project: PerfCtrs
ms.assetid: 9ed4f890-6256-45fd-a310-b5963a6131ae
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: "*PPERF_OBJECT_TYPE, PERF_DETAIL_ADVANCED, PERF_DETAIL_EXPERT, PERF_DETAIL_NOVICE, PERF_DETAIL_WIZARD, PERF_OBJECT_TYPE, PERF_OBJECT_TYPE structure [Perf], _PERF_OBJECT_TYPE, _win32_perf_object_type_str, base.perf_object_type_str, perf.perf_object_type_str, winperf/PERF_OBJECT_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winperf.h
api_name:
-	PERF_OBJECT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PERF_OBJECT_TYPE structure


## -description



			Describes object-specific performance information, for example, the number of instances of the object and the number of counters that the object defines.


## -struct-fields




### -field TotalByteLength

Size of the object-specific data, in bytes. This member is the offset from the beginning of this structure to the next 
<b>PERF_OBJECT_TYPE</b> structure, if one exists.


### -field DefinitionLength

Size of this structure plus the size of all the  
<a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a> structures.

If the object is a multiple instance object (the <b>NumInstances</b> member is not zero), this member is the offset from the beginning of this structure to the first 
<a href="https://msdn.microsoft.com/5ea617d3-857d-4e0a-ad10-4d63044fc927">PERF_INSTANCE_DEFINITION</a> structure. Otherwise, this value is the offset to the <a href="https://msdn.microsoft.com/5cff6142-6d71-46a5-a943-3ec91ebac62b">PERF_COUNTER_BLOCK</a>.


### -field HeaderLength

Size of this structure, in bytes. This member is the offset from the beginning of this structure to the first 
<a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a> structure.


### -field ObjectNameTitleIndex

Index to the object's name in the title database. For details on using the index to retrieve the object's name, see <a href="https://msdn.microsoft.com/9ddd1672-61cf-41c2-bec0-0d2b775bf970">Retrieving Counter Names and Help Text</a>.

Providers specify the index value in their initialization file. For details, see <a href="https://msdn.microsoft.com/6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4">Adding Counter Names and Descriptions to the Registry</a>.


### -field ObjectNameTitle

Reserved.


### -field ObjectHelpTitleIndex

Index to the object's help text in the title database.  For details on using the index to retrieve the object's help text, see <a href="https://msdn.microsoft.com/9ddd1672-61cf-41c2-bec0-0d2b775bf970">Retrieving Counter Names and Help Text</a>.

Providers specify the index value in their initialization file. For details, see <a href="https://msdn.microsoft.com/6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4">Adding Counter Names and Descriptions to the Registry</a>.


### -field ObjectHelpTitle

Reserved.


### -field DetailLevel

Level of detail. Consumers use this value to control display complexity. This value is the minimum detail level of all the counters for a given object. This member can be one of the following values. 



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
 


### -field NumCounters

Number of <a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a> blocks returned by the object.


### -field DefaultCounter

Index to the counter's name in the title database of the default counter whose information is to be displayed when this object is selected in the Performance tool. This member may be –1 to indicate that there is no default.


### -field NumInstances

Number of object instances for which counters are being provided. If the object can have zero or more instances, but has none at present, this value should be zero. If the object cannot have multiple instances, this value should be PERF_NO_INSTANCES.


### -field CodePage

This member is zero if the instance strings are Unicode strings. Otherwise, this member is the code-page identifier of the instance names. You can use the code-page value when calling <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> to convert the string to Unicode.


### -field PerfTime

Provider generated timestamp that consumers use when calculating counter values. For example, this could be the current value, in counts, of the high-resolution performance counter.

Providers need to provide this value if the counter types of their counters include the <b>PERF_OBJECT_TIMER</b> flag. Otherwise, consumers use the <b>PerfTime</b> value from <a href="https://msdn.microsoft.com/29f89719-7597-4f7b-879e-1670386f8396">PERF_DATA_BLOCK</a>.


### -field PerfFreq

Provider generated frequency value that consumers use when calculating counter values. For example, this could be the current frequency, in counts per second, of the high-resolution performance counter.

Providers need to provide this value if the counter types of their counters include the <b>PERF_OBJECT_TIMER</b> flag. Otherwise, consumers use the <b>PerfFreq</b> value from <a href="https://msdn.microsoft.com/29f89719-7597-4f7b-879e-1670386f8396">PERF_DATA_BLOCK</a>.


## -remarks



Providers use this structure to provide performance data for objects that they support. Consumers use this structure to consume performance data for objects that they queried.

 This structure is followed by a list of 
<a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a> structures, one for each counter defined for the performance object.
		For details on the layout of the performance data block, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.




## -see-also




<a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a>



<a href="https://msdn.microsoft.com/29f89719-7597-4f7b-879e-1670386f8396">PERF_DATA_BLOCK</a>



<a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>
 

 

