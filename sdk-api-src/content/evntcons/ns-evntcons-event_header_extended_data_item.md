---
UID: NS:evntcons._EVENT_HEADER_EXTENDED_DATA_ITEM
title: EVENT_HEADER_EXTENDED_DATA_ITEM (evntcons.h)
description: The EVENT_HEADER_EXTENDED_DATA_ITEM structure (evntcons.h) defines the extended data that ETW collects as part of the event data.
helpviewer_keywords: ["*PEVENT_HEADER_EXTENDED_DATA_ITEM","EVENT_HEADER_EXTENDED_DATA_ITEM","EVENT_HEADER_EXTENDED_DATA_ITEM structure [ETW]","EVENT_HEADER_EXT_TYPE_EVENT_KEY","EVENT_HEADER_EXT_TYPE_EVENT_SCHEMA_TL","EVENT_HEADER_EXT_TYPE_INSTANCE_INFO","EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY","EVENT_HEADER_EXT_TYPE_PROV_TRAITS","EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID","EVENT_HEADER_EXT_TYPE_SID","EVENT_HEADER_EXT_TYPE_STACK_TRACE32","EVENT_HEADER_EXT_TYPE_STACK_TRACE64","EVENT_HEADER_EXT_TYPE_TS_ID","PEVENT_HEADER_EXTENDED_DATA_ITEM","PEVENT_HEADER_EXTENDED_DATA_ITEM structure pointer [ETW]","_EVENT_HEADER_EXTENDED_DATA_ITEM","base.event_header_extended_data_item","etw.event_header_extended_data_item","relogger/EVENT_HEADER_EXTENDED_DATA_ITEM","relogger/PEVENT_HEADER_EXTENDED_DATA_ITEM"]
old-location: etw\event_header_extended_data_item.htm
tech.root: ETW
ms.assetid: 130dc14b-7488-48ab-a31d-310c0f4ee13f
ms.date: 10/22/2024
ms.keywords: '*PEVENT_HEADER_EXTENDED_DATA_ITEM, EVENT_HEADER_EXTENDED_DATA_ITEM, EVENT_HEADER_EXTENDED_DATA_ITEM structure [ETW], EVENT_HEADER_EXT_TYPE_EVENT_KEY, EVENT_HEADER_EXT_TYPE_EVENT_SCHEMA_TL, EVENT_HEADER_EXT_TYPE_INSTANCE_INFO, EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY, EVENT_HEADER_EXT_TYPE_PROV_TRAITS, EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID, EVENT_HEADER_EXT_TYPE_SID, EVENT_HEADER_EXT_TYPE_STACK_TRACE32, EVENT_HEADER_EXT_TYPE_STACK_TRACE64, EVENT_HEADER_EXT_TYPE_TS_ID, PEVENT_HEADER_EXTENDED_DATA_ITEM, PEVENT_HEADER_EXTENDED_DATA_ITEM structure pointer [ETW], _EVENT_HEADER_EXTENDED_DATA_ITEM, base.event_header_extended_data_item, etw.event_header_extended_data_item, relogger/EVENT_HEADER_EXTENDED_DATA_ITEM, relogger/PEVENT_HEADER_EXTENDED_DATA_ITEM'
req.header: evntcons.h
req.include-header: Evntcons.h
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
req.typenames: EVENT_HEADER_EXTENDED_DATA_ITEM, *PEVENT_HEADER_EXTENDED_DATA_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_HEADER_EXTENDED_DATA_ITEM
 - evntcons/_EVENT_HEADER_EXTENDED_DATA_ITEM
 - PEVENT_HEADER_EXTENDED_DATA_ITEM
 - evntcons/PEVENT_HEADER_EXTENDED_DATA_ITEM
 - EVENT_HEADER_EXTENDED_DATA_ITEM
 - evntcons/EVENT_HEADER_EXTENDED_DATA_ITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - EVENT_HEADER_EXTENDED_DATA_ITEM
---

# EVENT_HEADER_EXTENDED_DATA_ITEM structure (evntcons.h)

## -description

Defines the extended data that Event Tracing for Windows (ETW) collects as part of the event data.

## -struct-fields

### -field Reserved1

Reserved.

### -field ExtType

The type of extended data. The following examples are some possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_EVENT_KEY"></a><a id="event_header_ext_type_event_key"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_EVENT_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an EVENT_EXTENDED_ITEM_EVENT_KEY structure containing a unique event identifier that is a 64-bit scalar.

The <b>EnableProperty</b> EVENT_ENABLE_PROPERTY_EVENT_KEY needs to be passed in for the <a href="/windows/desktop/ETW/enabletrace">EnableTrace</a> call for a given provider to enable this feature.

</td>
</tr>

<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_EVENT_SCHEMA_TL"></a><a id="event_header_ext_type_event_schema_tl"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_EVENT_SCHEMA_TL</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an extended header item that contains TraceLogging event metadata information.

</td>
</tr>


<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_INSTANCE_INFO"></a><a id="event_header_ext_type_instance_info"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_INSTANCE_INFO</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="/windows/desktop/api/evntcons/ns-evntcons-event_extended_item_instance">EVENT_EXTENDED_ITEM_INSTANCE</a> structure that contains the activity identifier if you called <a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> to write the event.

</td>
</tr>

<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_PMC_COUNTERS"></a><a id="event_header_ext_type_pmc_counters"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_PMC_COUNTERS</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="/windows/win32/api/evntcons/ns-evntcons-event_extended_item_pmc_counters">EVENT_EXTENDED_ITEM_PMC_COUNTERS</a> structure that contains the current PMC Counter values. To enable this feature, the valid PMC counters for the CPU must be set via <a href="/windows/win32/api/evntrace/nf-evntrace-tracesetinformation">TraceSetInformation</a>, with valid <b>Source</b> values found by calling <a href="/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation">TraceQueryInformation</a> with <a href="/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class">TraceProfileSourceListInfo</a>.

</td>
</tr>


<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY"></a><a id="event_header_ext_type_process_start_key"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an EVENT_EXTENDED_ITEM_PROCESS_START_KEY structure that contains a unique process identifier (unique across the boot session). This identifier is a 64-bit scalar. 

The <b>EnableProperty</b> EVENT_ENABLE_PROPERTY_PROCESS_START_KEY needs to be passed in for the <a href="/windows/desktop/ETW/enabletrace">EnableTrace</a> call for a given provider to enable this feature. 

</td>
</tr>

<tr>
<td width="40%"><a id="_EVENT_HEADER_EXT_TYPE_PROV_TRAITS"></a><a id="_event_header_ext_type_prov_traits"></a><dl>
<dt><b>	EVENT_HEADER_EXT_TYPE_PROV_TRAITS</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an extended header item that  contains provider traits data, for example traits set through <a href="/windows/desktop/api/evntprov/nf-evntprov-eventsetinformation">EventSetInformation(EventProviderSetTraits)</a> or specified through <a href="/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor">EVENT_DATA_DESCRIPTOR_TYPE_PROVIDER_METADATA</a>.

</td>
</tr>

<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID"></a><a id="event_header_ext_type_related_activityid"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="/windows/win32/api/evntcons/ns-evntcons-event_extended_item_related_activityid">EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID</a> structure that contains the related activity identifier if you called <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a> to write the event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_SID"></a><a id="event_header_ext_type_sid"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_SID</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that contains the security identifier (SID) of the user that logged the event. ETW includes the SID if you set the <i>EnableProperty</i> parameter of <a href="/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> to EVENT_ENABLE_PROPERTY_SID.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_STACK_TRACE32"></a><a id="event_header_ext_type_stack_trace32"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_STACK_TRACE32</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="/windows/win32/api/evntcons/ns-evntcons-event_extended_item_stack_trace32">EVENT_EXTENDED_ITEM_STACK_TRACE32</a> structure that contains the call stack if the event is captured on a 32-bit computer.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_STACK_TRACE64"></a><a id="event_header_ext_type_stack_trace64"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_STACK_TRACE64</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="/windows/win32/api/evntcons/ns-evntcons-event_extended_item_stack_trace64">EVENT_EXTENDED_ITEM_STACK_TRACE64</a> structure that contains the call stack if the event is captured on a 64-bit computer.

</td>
</tr>
</tr>


<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_TS_ID"></a><a id="event_header_ext_type_ts_id"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_TS_ID</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="/windows/desktop/api/evntcons/ns-evntcons-event_extended_item_ts_id">EVENT_EXTENDED_ITEM_TS_ID</a> structure that contains the terminal session identifier. ETW includes the terminal session identifier if you set the <i>EnableProperty</i> parameter of <a href="/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> to EVENT_ENABLE_PROPERTY_TS_ID.

</td>
</tr>


</table>

### -field Linkage

Reserved.

### -field Reserved2

Reserved.

### -field DataSize

Size, in bytes, of the extended data that <b>DataPtr</b> points to.

### -field DataPtr

Pointer to the extended data. The <b>ExtType</b> member determines the type of extended data to which this member points.

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a>
