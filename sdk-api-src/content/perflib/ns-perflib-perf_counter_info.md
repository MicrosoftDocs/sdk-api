---
UID: NS:perflib._PERF_COUNTER_INFO
title: PERF_COUNTER_INFO (perflib.h)
description: Defines information about a counter that a provider uses. The CTRPP tool automatically generates this structure based on the schema you specify.
helpviewer_keywords: ["*PPERF_COUNTER_INFO","PERF_ATTRIB_BY_REFERENCE","PERF_ATTRIB_DISPLAY_AS_HEX","PERF_ATTRIB_DISPLAY_AS_REAL","PERF_ATTRIB_NO_DISPLAYABLE","PERF_ATTRIB_NO_GROUP_SEPARATOR","PERF_COUNTER_INFO","PERF_COUNTER_INFO structure [Perf]","PERF_COUNTER_INFO","*PPERF_COUNTER_INFO","PERF_COUNTER_INFO","*PPERF_COUNTER_INFO structure [Perf]","PERF_DETAIL_ADVANCED","PERF_DETAIL_NOVICE","base.perf_counter_info","perf.perf_counter_info","perflib/PERF_COUNTER_INFO"]
old-location: perf\perf_counter_info.htm
tech.root: perf
ms.assetid: f1fb6ad5-ad38-46d0-b76d-803887ba3d97
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTER_INFO, PERF_ATTRIB_BY_REFERENCE, PERF_ATTRIB_DISPLAY_AS_HEX, PERF_ATTRIB_DISPLAY_AS_REAL, PERF_ATTRIB_NO_DISPLAYABLE, PERF_ATTRIB_NO_GROUP_SEPARATOR, PERF_COUNTER_INFO, PERF_COUNTER_INFO structure [Perf], PERF_COUNTER_INFO,*PPERF_COUNTER_INFO, PERF_COUNTER_INFO,*PPERF_COUNTER_INFO structure [Perf], PERF_DETAIL_ADVANCED, PERF_DETAIL_NOVICE, base.perf_counter_info, perf.perf_counter_info, perflib/PERF_COUNTER_INFO'
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PERF_COUNTER_INFO, *PPERF_COUNTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTER_INFO
 - perflib/_PERF_COUNTER_INFO
 - PPERF_COUNTER_INFO
 - perflib/PPERF_COUNTER_INFO
 - PERF_COUNTER_INFO
 - perflib/PERF_COUNTER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_COUNTER_INFO, *PPERF_COUNTER_INFO
---

# PERF_COUNTER_INFO structure


## -description

Defines information about a counter that a provider uses.  The <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool automatically generates this structure based on the  schema you specify.

## -struct-fields

### -field CounterId

Identifier that uniquely identifies the counter within the counter set.

### -field Type

Specifies the type of counter. For possible counter types, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.

### -field Attrib

One or more attributes that indicate how to display this counter.


The possible values are:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_ATTRIB_BY_REFERENCE"></a><a id="perf_attrib_by_reference"></a><dl>
<dt><b>PERF_ATTRIB_BY_REFERENCE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the value of the counter by reference as opposed to by value.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_ATTRIB_NO_DISPLAYABLE"></a><a id="perf_attrib_no_displayable"></a><dl>
<dt><b>PERF_ATTRIB_NO_DISPLAYABLE</b></dt>
</dl>
</td>
<td width="60%">
Do not display the counter value. 

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_ATTRIB_NO_GROUP_SEPARATOR"></a><a id="perf_attrib_no_group_separator"></a><dl>
<dt><b>PERF_ATTRIB_NO_GROUP_SEPARATOR</b></dt>
</dl>
</td>
<td width="60%">
Do not use digit separators when displaying counter value. 

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_ATTRIB_DISPLAY_AS_REAL"></a><a id="perf_attrib_display_as_real"></a><dl>
<dt><b>PERF_ATTRIB_DISPLAY_AS_REAL</b></dt>
</dl>
</td>
<td width="60%">
Display the counter value as a real value.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_ATTRIB_DISPLAY_AS_HEX"></a><a id="perf_attrib_display_as_hex"></a><dl>
<dt><b>PERF_ATTRIB_DISPLAY_AS_HEX</b></dt>
</dl>
</td>
<td width="60%">
Display the counter value as a hexadecimal number. 

</td>
</tr>
</table>
 

The attributes PERF_ATTRIB_NO_GROUP_SEPARATOR, PERF_ATTRIB_DISPLAY_AS_REAL, and PERF_ATTRIB_DISPLAY_AS_HEX are not mutually exclusive. If you specify all three attributes, precedence is given to the attributes in the order given.

### -field Size

Size, in bytes, of this structure.

### -field DetailLevel

Specify the target audience for the counter. 


Possible values are:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_NOVICE"></a><a id="perf_detail_novice"></a><dl>
<dt><b>PERF_DETAIL_NOVICE</b></dt>
</dl>
</td>
<td width="60%">
You can display the counter to any level of user.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_ADVANCED"></a><a id="perf_detail_advanced"></a><dl>
<dt><b>PERF_DETAIL_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
The counter is complicated and should be displayed only to advanced users.

</td>
</tr>
</table>

### -field Scale

Scale factor to apply to the counter value. Valid values range from –10 through 10. Zero if no scale is applied. If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is –1, the scale value is .10; and so on.

### -field Offset

Byte offset from the beginning of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> block to the counter value.

## -remarks

This structure is contained within a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_info">PERF_COUNTERSET_INFO</a> or <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> block.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_info">PERF_COUNTERSET_INFO</a>



<a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a>