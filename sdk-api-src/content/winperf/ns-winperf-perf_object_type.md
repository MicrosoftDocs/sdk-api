---
UID: NS:winperf._PERF_OBJECT_TYPE
title: PERF_OBJECT_TYPE (winperf.h)
description: Describes object-specific performance information, for example, the number of instances of the object and the number of counters that the object defines.
helpviewer_keywords: ["*PPERF_OBJECT_TYPE","PERF_DETAIL_ADVANCED","PERF_DETAIL_EXPERT","PERF_DETAIL_NOVICE","PERF_DETAIL_WIZARD","PERF_OBJECT_TYPE","PERF_OBJECT_TYPE structure [Perf]","_win32_perf_object_type_str","base.perf_object_type_str","perf.perf_object_type_str","winperf/PERF_OBJECT_TYPE"]
old-location: perf\perf_object_type_str.htm
tech.root: perf
ms.assetid: 9ed4f890-6256-45fd-a310-b5963a6131ae
ms.date: 12/05/2018
ms.keywords: '*PPERF_OBJECT_TYPE, PERF_DETAIL_ADVANCED, PERF_DETAIL_EXPERT, PERF_DETAIL_NOVICE, PERF_DETAIL_WIZARD, PERF_OBJECT_TYPE, PERF_OBJECT_TYPE structure [Perf], _win32_perf_object_type_str, base.perf_object_type_str, perf.perf_object_type_str, winperf/PERF_OBJECT_TYPE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_OBJECT_TYPE
 - winperf/_PERF_OBJECT_TYPE
 - PPERF_OBJECT_TYPE
 - winperf/PPERF_OBJECT_TYPE
 - PERF_OBJECT_TYPE
 - winperf/PERF_OBJECT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winperf.h
api_name:
 - PERF_OBJECT_TYPE
---

# PERF_OBJECT_TYPE structure


## -description

Describes object-specific performance information, for example, the number of instances of the object and the number of counters that the object defines.

## -struct-fields

### -field TotalByteLength

Size of the object-specific data, in bytes. This member is the offset from the beginning of this structure to the next 
<b>PERF_OBJECT_TYPE</b> structure, if one exists.

### -field DefinitionLength

Size of this structure plus the size of all the  
<a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a> structures.

If the object is a multiple instance object (the <b>NumInstances</b> member is not zero), this member is the offset from the beginning of this structure to the first 
<a href="/windows/desktop/api/winperf/ns-winperf-perf_instance_definition">PERF_INSTANCE_DEFINITION</a> structure. Otherwise, this value is the offset to the <a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_block">PERF_COUNTER_BLOCK</a>.

### -field HeaderLength

Size of this structure, in bytes. This member is the offset from the beginning of this structure to the first 
<a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a> structure.

### -field ObjectNameTitleIndex

Index to the object's name in the title database. For details on using the index to retrieve the object's name, see <a href="/windows/win32/perfctrs/retrieving-counter-names-and-help-text">Retrieving Counter Names and Help Text</a>.

Providers specify the index value in their initialization file. For details, see <a href="/windows/desktop/PerfCtrs/adding-counter-names-and-descriptions-to-the-registry">Adding Counter Names and Descriptions to the Registry</a>.

### -field ObjectNameTitle

Reserved.

### -field ObjectHelpTitleIndex

Index to the object's help text in the title database.  For details on using the index to retrieve the object's help text, see <a href="/windows/win32/perfctrs/retrieving-counter-names-and-help-text">Retrieving Counter Names and Help Text</a>.

Providers specify the index value in their initialization file. For details, see <a href="/windows/desktop/PerfCtrs/adding-counter-names-and-descriptions-to-the-registry">Adding Counter Names and Descriptions to the Registry</a>.

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

Number of <a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a> blocks returned by the object.

### -field DefaultCounter

Index to the counter's name in the title database of the default counter whose information is to be displayed when this object is selected in the Performance tool. This member may be –1 to indicate that there is no default.

### -field NumInstances

Number of object instances for which counters are being provided. If the object can have zero or more instances, but has none at present, this value should be zero. If the object cannot have multiple instances, this value should be PERF_NO_INSTANCES.

### -field CodePage

This member is zero if the instance strings are Unicode strings. Otherwise, this member is the code-page identifier of the instance names. You can use the code-page value when calling <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> to convert the string to Unicode.

### -field PerfTime

Provider generated timestamp that consumers use when calculating counter values. For example, this could be the current value, in counts, of the high-resolution performance counter.

Providers need to provide this value if the counter types of their counters include the <b>PERF_OBJECT_TIMER</b> flag. Otherwise, consumers use the <b>PerfTime</b> value from <a href="/windows/desktop/api/winperf/ns-winperf-perf_data_block">PERF_DATA_BLOCK</a>.

### -field PerfFreq

Provider generated frequency value that consumers use when calculating counter values. For example, this could be the current frequency, in counts per second, of the high-resolution performance counter.

Providers need to provide this value if the counter types of their counters include the <b>PERF_OBJECT_TIMER</b> flag. Otherwise, consumers use the <b>PerfFreq</b> value from <a href="/windows/desktop/api/winperf/ns-winperf-perf_data_block">PERF_DATA_BLOCK</a>.

## -remarks

Providers use this structure to provide performance data for objects that they support. Consumers use this structure to consume performance data for objects that they queried.

 This structure is followed by a list of 
<a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a> structures, one for each counter defined for the performance object.
		For details on the layout of the performance data block, see <a href="/windows/desktop/PerfCtrs/performance-data-format">Performance Data Format</a>.

## -see-also

<a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a>



<a href="/windows/desktop/api/winperf/ns-winperf-perf_data_block">PERF_DATA_BLOCK</a>



<a href="/windows/desktop/PerfCtrs/performance-data-format">Performance Data Format</a>