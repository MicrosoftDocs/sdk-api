---
UID: NS:perflib._PERF_COUNTER_INFO
title: "_PERF_COUNTER_INFO"
author: windows-driver-content
description: Defines information about a counter that a provider uses. The CTRPP tool automatically generates this structure based on the schema you specify.
old-location: perf\perf_counter_info.htm
old-project: PerfCtrs
ms.assetid: f1fb6ad5-ad38-46d0-b76d-803887ba3d97
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PPERF_COUNTER_INFO, PERF_ATTRIB_BY_REFERENCE, PERF_ATTRIB_DISPLAY_AS_HEX, PERF_ATTRIB_DISPLAY_AS_REAL, PERF_ATTRIB_NO_DISPLAYABLE, PERF_ATTRIB_NO_GROUP_SEPARATOR, PERF_COUNTER_INFO, PERF_COUNTER_INFO structure [Perf], PERF_COUNTER_INFO,*PPERF_COUNTER_INFO, PERF_COUNTER_INFO,*PPERF_COUNTER_INFO structure [Perf], PERF_DETAIL_ADVANCED, PERF_DETAIL_NOVICE, _PERF_COUNTER_INFO, base.perf_counter_info, perf.perf_counter_info, perflib/PERF_COUNTER_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PERF_COUNTER_INFO, *PPERF_COUNTER_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Perflib.h
api_name:
-	PERF_COUNTER_INFO, *PPERF_COUNTER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _PERF_COUNTER_INFO structure


## -description


Defines information about a counter that a provider uses.  The <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool automatically generates this structure based on the  schema you specify.


## -struct-fields




### -field CounterId

Identifier that uniquely identifies the counter within the counter set.


### -field Type

Specifies the type of counter. For possible counter types, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84422">Counter Types</a> in the Windows 2003 Deployment Guide.


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

Byte offset from the beginning of the <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> block to the counter value.


## -remarks



This structure is contained within a <a href="https://msdn.microsoft.com/bf48dcdb-6fdd-4093-9006-a53690c3ed86">PERF_COUNTERSET_INFO</a> or <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> block.




## -see-also




<a href="https://msdn.microsoft.com/bf48dcdb-6fdd-4093-9006-a53690c3ed86">PERF_COUNTERSET_INFO</a>



<a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a>
 

 

