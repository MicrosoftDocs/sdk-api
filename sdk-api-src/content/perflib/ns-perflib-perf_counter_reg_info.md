---
UID: NS:perflib._PERF_COUNTER_REG_INFO
title: PERF_COUNTER_REG_INFO (perflib.h)
description: Provides registration information about a performance counter.
helpviewer_keywords: ["*PPERF_COUNTER_REG_INFO","PERF_100NSEC_MULTI_TIMER","PERF_100NSEC_MULTI_TIMER_II","PERF_100NSEC_TIMER","PERF_100NSEC_TIMER_INV","PERF_AGGREGATE_AVG","PERF_AGGREGATE_MAX","PERF_AGGREGATE_MIN","PERF_AGGREGATE_TOTAL","PERF_AGGREGATE_UNDEFINED","PERF_ATTRIB_BY_REFERENCE","PERF_ATTRIB_DISPLAY_AS_HEX","PERF_ATTRIB_DISPLAY_AS_REAL","PERF_ATTRIB_NO_DISPLAYABLE","PERF_ATTRIB_NO_GROUP_SEPARATOR","PERF_AVERAGE_BASE","PERF_AVERAGE_BULK","PERF_AVERAGE_TIMER","PERF_COUNTER_100NS_QUEUELEN_TYPE","PERF_COUNTER_BULK_COUNT","PERF_COUNTER_COUNTER","PERF_COUNTER_DELTA","PERF_COUNTER_LARGE_DELTA","PERF_COUNTER_LARGE_QUEUELEN_TYPE","PERF_COUNTER_LARGE_RAWCOUNT","PERF_COUNTER_LARGE_RAWCOUNT_HEX","PERF_COUNTER_MULTI_TIMER","PERF_COUNTER_MULTI_TIMER_INV","PERF_COUNTER_OBJ_QUEUELEN_TYPE","PERF_COUNTER_RAWCOUNT","PERF_COUNTER_RAWCOUNT_HEX","PERF_COUNTER_REG_INFO","PERF_COUNTER_REG_INFO structure [Perf]","PERF_COUNTER_TEXT","PERF_COUNTER_TIMER","PERF_COUNTER_TIMER_INV","PERF_DETAIL_ADVANCED","PERF_DETAIL_NOVICE","PERF_ELAPSED_TIME","PERF_LARGE_RAW_BASE","PERF_OBJ_TIME_TIMER","PERF_PRECISION_100NS_TIMER","PERF_PRECISION_OBJECT_TIMER","PERF_PRECISION_TIMER","PERF_RAW_BASE","PERF_RAW_FRACTION","PERF_SAMPLE_COUNTER","PERF_SAMPLE_FRACTION","PPERF_COUNTER_REG_INFO","PPERF_COUNTER_REG_INFO structure pointer [Perf]","perf.perf_counter_reg_info","perflib/PERF_COUNTER_REG_INFO","perflib/PPERF_COUNTER_REG_INFO"]
old-location: perf\perf_counter_reg_info.htm
tech.root: perf
ms.assetid: 34CA6EA3-DF74-4DB5-8DD0-2B0BB0162F9D
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTER_REG_INFO, PERF_100NSEC_MULTI_TIMER, PERF_100NSEC_MULTI_TIMER_II, PERF_100NSEC_TIMER, PERF_100NSEC_TIMER_INV, PERF_AGGREGATE_AVG, PERF_AGGREGATE_MAX, PERF_AGGREGATE_MIN, PERF_AGGREGATE_TOTAL, PERF_AGGREGATE_UNDEFINED, PERF_ATTRIB_BY_REFERENCE, PERF_ATTRIB_DISPLAY_AS_HEX, PERF_ATTRIB_DISPLAY_AS_REAL, PERF_ATTRIB_NO_DISPLAYABLE, PERF_ATTRIB_NO_GROUP_SEPARATOR, PERF_AVERAGE_BASE, PERF_AVERAGE_BULK, PERF_AVERAGE_TIMER, PERF_COUNTER_100NS_QUEUELEN_TYPE, PERF_COUNTER_BULK_COUNT, PERF_COUNTER_COUNTER, PERF_COUNTER_DELTA, PERF_COUNTER_LARGE_DELTA, PERF_COUNTER_LARGE_QUEUELEN_TYPE, PERF_COUNTER_LARGE_RAWCOUNT, PERF_COUNTER_LARGE_RAWCOUNT_HEX, PERF_COUNTER_MULTI_TIMER, PERF_COUNTER_MULTI_TIMER_INV, PERF_COUNTER_OBJ_QUEUELEN_TYPE, PERF_COUNTER_RAWCOUNT, PERF_COUNTER_RAWCOUNT_HEX, PERF_COUNTER_REG_INFO, PERF_COUNTER_REG_INFO structure [Perf], PERF_COUNTER_TEXT, PERF_COUNTER_TIMER, PERF_COUNTER_TIMER_INV, PERF_DETAIL_ADVANCED, PERF_DETAIL_NOVICE, PERF_ELAPSED_TIME, PERF_LARGE_RAW_BASE, PERF_OBJ_TIME_TIMER, PERF_PRECISION_100NS_TIMER, PERF_PRECISION_OBJECT_TIMER, PERF_PRECISION_TIMER, PERF_RAW_BASE, PERF_RAW_FRACTION, PERF_SAMPLE_COUNTER, PERF_SAMPLE_FRACTION, PPERF_COUNTER_REG_INFO, PPERF_COUNTER_REG_INFO structure pointer [Perf], perf.perf_counter_reg_info, perflib/PERF_COUNTER_REG_INFO, perflib/PPERF_COUNTER_REG_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PERF_COUNTER_REG_INFO, *PPERF_COUNTER_REG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTER_REG_INFO
 - perflib/_PERF_COUNTER_REG_INFO
 - PPERF_COUNTER_REG_INFO
 - perflib/PPERF_COUNTER_REG_INFO
 - PERF_COUNTER_REG_INFO
 - perflib/PERF_COUNTER_REG_INFO
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
 - PERF_COUNTER_REG_INFO
---

# PERF_COUNTER_REG_INFO structure


## -description

Provides registration information about a performance counter.

## -struct-fields

### -field CounterId

A unique identifier for the performance counter within the counter set. A counter set can contain a maximum of 64,000 performance counters.

### -field Type

The type of the performance counter. For information about the predefined counter types, see the Counter Types section of the <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Windows Server 2003 Deployment Kit</a>. Consumers use the counter type to determine how to calculate and display the counter value. Providers should limit their choice of counter types to the predefined list. 
					


The possible values are:



<a id="PERF_100NSEC_MULTI_TIMER"></a>
<a id="perf_100nsec_multi_timer"></a>


#### PERF_100NSEC_MULTI_TIMER

<a id="PERF_100NSEC_MULTI_TIMER_II"></a>
<a id="perf_100nsec_multi_timer_ii"></a>


#### PERF_100NSEC_MULTI_TIMER_II

<a id="PERF_100NSEC_TIMER"></a>
<a id="perf_100nsec_timer"></a>


#### PERF_100NSEC_TIMER

<a id="PERF_100NSEC_TIMER_INV"></a>
<a id="perf_100nsec_timer_inv"></a>


#### PERF_100NSEC_TIMER_INV

<a id="PERF_AVERAGE_BASE"></a>
<a id="perf_average_base"></a>


#### PERF_AVERAGE_BASE

<a id="PERF_AVERAGE_BULK"></a>
<a id="perf_average_bulk"></a>


#### PERF_AVERAGE_BULK

<a id="PERF_AVERAGE_TIMER"></a>
<a id="perf_average_timer"></a>


#### PERF_AVERAGE_TIMER

<a id="PERF_COUNTER_100NS_QUEUELEN_TYPE"></a>
<a id="perf_counter_100ns_queuelen_type"></a>


#### PERF_COUNTER_100NS_QUEUELEN_TYPE

<a id="PERF_COUNTER_BULK_COUNT"></a>
<a id="perf_counter_bulk_count"></a>


#### PERF_COUNTER_BULK_COUNT

<a id="PERF_COUNTER_COUNTER"></a>
<a id="perf_counter_counter"></a>


#### PERF_COUNTER_COUNTER

<a id="PERF_COUNTER_DELTA"></a>
<a id="perf_counter_delta"></a>


#### PERF_COUNTER_DELTA

<a id="PERF_COUNTER_LARGE_DELTA"></a>
<a id="perf_counter_large_delta"></a>


#### PERF_COUNTER_LARGE_DELTA

<a id="PERF_COUNTER_LARGE_QUEUELEN_TYPE"></a>
<a id="perf_counter_large_queuelen_type"></a>


#### PERF_COUNTER_LARGE_QUEUELEN_TYPE

<a id="PERF_COUNTER_LARGE_RAWCOUNT"></a>
<a id="perf_counter_large_rawcount"></a>


#### PERF_COUNTER_LARGE_RAWCOUNT

<a id="PERF_COUNTER_LARGE_RAWCOUNT_HEX"></a>
<a id="perf_counter_large_rawcount_hex"></a>


#### PERF_COUNTER_LARGE_RAWCOUNT_HEX

<a id="PERF_COUNTER_MULTI_TIMER"></a>
<a id="perf_counter_multi_timer"></a>


#### PERF_COUNTER_MULTI_TIMER

<a id="PERF_COUNTER_MULTI_TIMER_INV"></a>
<a id="perf_counter_multi_timer_inv"></a>


#### PERF_COUNTER_MULTI_TIMER_INV

<a id="PERF_COUNTER_OBJ_QUEUELEN_TYPE"></a>
<a id="perf_counter_obj_queuelen_type"></a>


#### PERF_COUNTER_OBJ_QUEUELEN_TYPE

<a id="PERF_COUNTER_RAWCOUNT"></a>
<a id="perf_counter_rawcount"></a>


#### PERF_COUNTER_RAWCOUNT

<a id="PERF_COUNTER_RAWCOUNT_HEX"></a>
<a id="perf_counter_rawcount_hex"></a>


#### PERF_COUNTER_RAWCOUNT_HEX

<a id="PERF_COUNTER_TEXT"></a>
<a id="perf_counter_text"></a>


#### PERF_COUNTER_TEXT

<a id="PERF_COUNTER_TIMER"></a>
<a id="perf_counter_timer"></a>


#### PERF_COUNTER_TIMER

<a id="PERF_COUNTER_TIMER_INV"></a>
<a id="perf_counter_timer_inv"></a>


#### PERF_COUNTER_TIMER_INV

<a id="PERF_ELAPSED_TIME"></a>
<a id="perf_elapsed_time"></a>


#### PERF_ELAPSED_TIME

<a id="PERF_LARGE_RAW_BASE"></a>
<a id="perf_large_raw_base"></a>


#### PERF_LARGE_RAW_BASE

<a id="PERF_OBJ_TIME_TIMER"></a>
<a id="perf_obj_time_timer"></a>


#### PERF_OBJ_TIME_TIMER

<a id="PERF_PRECISION_100NS_TIMER"></a>
<a id="perf_precision_100ns_timer"></a>


#### PERF_PRECISION_100NS_TIMER

<a id="PERF_PRECISION_TIMER"></a>
<a id="perf_precision_timer"></a>


#### PERF_PRECISION_TIMER

<a id="PERF_PRECISION_OBJECT_TIMER"></a>
<a id="perf_precision_object_timer"></a>


#### PERF_PRECISION_OBJECT_TIMER

<a id="PERF_RAW_BASE"></a>
<a id="perf_raw_base"></a>


#### PERF_RAW_BASE

<a id="PERF_RAW_FRACTION"></a>
<a id="perf_raw_fraction"></a>


#### PERF_RAW_FRACTION

<a id="PERF_SAMPLE_COUNTER"></a>
<a id="perf_sample_counter"></a>


#### PERF_SAMPLE_COUNTER

<a id="PERF_SAMPLE_FRACTION"></a>
<a id="perf_sample_fraction"></a>


#### PERF_SAMPLE_FRACTION

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
 

The attributes <b>PERF_ATTRIB_NO_GROUP_SEPARATOR</b>, <b>PERF_ATTRIB_DISPLAY_AS_REAL</b>, and <b>PERF_ATTRIB_DISPLAY_AS_HEX</b> are not mutually exclusive. If you specify all three attributes, precedence is given to the attributes in the order given.

### -field DetailLevel

The target audience for the counter. 


The possible values are:



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

### -field DefaultScale

The scaling factor to apply to the raw performance counter value. Valid values range from –10 through 10. Zero if no scale is applied. If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is –1, the scale value is .10; and so on. The scaled value of the performance counter is equal to the raw value of the performance counter multiplied by  10 raised to the power that the <b>DefaultScale</b> member specifies.

### -field BaseCounterId

The counter identifier of the base counter. 0xFFFFFFFF indicates that there is no base counter.

### -field PerfTimeId

The counter identifier of the performance counter. 0xFFFFFFFF indicates that there is no performance counter.

### -field PerfFreqId

The counter identifier of the frequency counter. 0xFFFFFFFF indicates that there is no frequency counter.

### -field MultiId

 The counter identifier of the multi-counter. 0xFFFFFFFF indicates that there is no multi-counter.

### -field AggregateFunc

The aggregation function the client should apply to the counter if the  

counter set to which the counter belongs is of type Global Aggregate, Multiple  

Instance Aggregate, or Global Aggregate History. The client specifies the  counter instances across which the aggregation is performed if the counter set type  

is Multiple Instance Aggregate; otherwise, the client must aggregate values  

across all instances of the counter set. One of the following values must be  

specified. 


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_AGGREGATE_UNDEFINED"></a><a id="perf_aggregate_undefined"></a><dl>
<dt><b>PERF_AGGREGATE_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_AGGREGATE_TOTAL"></a><a id="perf_aggregate_total"></a><dl>
<dt><b>PERF_AGGREGATE_TOTAL</b></dt>
</dl>
</td>
<td width="60%">
The sum of the values of the returned counter instances.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_AGGREGATE_AVG"></a><a id="perf_aggregate_avg"></a><dl>
<dt><b>PERF_AGGREGATE_AVG</b></dt>
</dl>
</td>
<td width="60%">
The average of the values of the returned counter instances.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_AGGREGATE_MIN"></a><a id="perf_aggregate_min"></a><dl>
<dt><b>PERF_AGGREGATE_MIN</b></dt>
</dl>
</td>
<td width="60%">
    The minimum value of the returned counter instance values. 


</td>
</tr>
<tr>
<td width="40%"><a id="PERF_AGGREGATE_MAX_"></a><a id="perf_aggregate_max_"></a><dl>
<dt><b>PERF_AGGREGATE_MAX </b></dt>
</dl>
</td>
<td width="60%">
    The maximum value of the returned counter instance values.


</td>
</tr>
</table>

### -field Reserved

Reserved.

## -remarks

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to <b>PERF_REG_COUNTERSET_STRUCT</b> gets a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_reg_info">PERF_COUNTERSET_REG_INFO</a> block that
contains one or more <b>PERF_COUNTER_REG_INFO</b> structures.



The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to 
<b>PERF_REG_COUNTER_STRUCT</b> gets a <b>PERF_COUNTER_REG_INFO</b> structure.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_reg_info">PERF_COUNTERSET_REG_INFO</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a>