---
UID: NS:relogger._EVENT_HEADER_EXTENDED_DATA_ITEM
title: "_EVENT_HEADER_EXTENDED_DATA_ITEM"
author: windows-sdk-content
description: Defines the extended data that ETW collects as part of the event data.
old-location: etw\event_header_extended_data_item.htm
tech.root: etw
ms.assetid: 130dc14b-7488-48ab-a31d-310c0f4ee13f
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PEVENT_HEADER_EXTENDED_DATA_ITEM, EVENT_HEADER_EXTENDED_DATA_ITEM, EVENT_HEADER_EXTENDED_DATA_ITEM structure [ETW], EVENT_HEADER_EXT_TYPE_EVENT_KEY, EVENT_HEADER_EXT_TYPE_EVENT_SCHEMA_TL, EVENT_HEADER_EXT_TYPE_INSTANCE_INFO, EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY, EVENT_HEADER_EXT_TYPE_PROV_TRAITS, EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID, EVENT_HEADER_EXT_TYPE_SID, EVENT_HEADER_EXT_TYPE_STACK_TRACE32, EVENT_HEADER_EXT_TYPE_STACK_TRACE64, EVENT_HEADER_EXT_TYPE_TS_ID, PEVENT_HEADER_EXTENDED_DATA_ITEM, PEVENT_HEADER_EXTENDED_DATA_ITEM structure pointer [ETW], _EVENT_HEADER_EXTENDED_DATA_ITEM, base.event_header_extended_data_item, etw.event_header_extended_data_item, relogger/EVENT_HEADER_EXTENDED_DATA_ITEM, relogger/PEVENT_HEADER_EXTENDED_DATA_ITEM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: relogger.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - EVENT_HEADER_EXTENDED_DATA_ITEM
product: Windows
targetos: Windows
req.typenames: EVENT_HEADER_EXTENDED_DATA_ITEM, *PEVENT_HEADER_EXTENDED_DATA_ITEM
req.redist: 
---

# _EVENT_HEADER_EXTENDED_DATA_ITEM structure


## -description


The <b>EVENT_HEADER_EXTENDED_DATA_ITEM</b> structure defines the extended data that ETW collects as part of the event data.


## -struct-fields




### -field Reserved1

Reserved.


### -field ExtType

Type of extended data. The following are possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID"></a><a id="event_header_ext_type_related_activityid"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_RELATED_ACTIVITYID</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="https://msdn.microsoft.com/cabc11ca-e65e-4ffd-9832-7fb4f77417e4">EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID</a> structure that contains the related activity identifier if you called <a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a> to write the event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_SID"></a><a id="event_header_ext_type_sid"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_SID</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that contains the security identifier (SID) of the user that logged the event. ETW includes the SID if you set the <i>EnableProperty</i> parameter of <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> to EVENT_ENABLE_PROPERTY_SID.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_TS_ID"></a><a id="event_header_ext_type_ts_id"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_TS_ID</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="https://msdn.microsoft.com/fcf1252d-9730-45a2-b601-60f76decd0dd">EVENT_EXTENDED_ITEM_TS_ID</a> structure that contains the terminal session identifier. ETW includes the terminal session identifier if you set the <i>EnableProperty</i> parameter of <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> to EVENT_ENABLE_PROPERTY_TS_ID.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_INSTANCE_INFO"></a><a id="event_header_ext_type_instance_info"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_INSTANCE_INFO</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="https://msdn.microsoft.com/3def638b-cab2-4b5d-b409-7285caa77ae1">EVENT_EXTENDED_ITEM_INSTANCE</a> structure that contains the activity identifier if you called <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> to write the event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_STACK_TRACE32"></a><a id="event_header_ext_type_stack_trace32"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_STACK_TRACE32</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="https://msdn.microsoft.com/6898951a-5719-47aa-a219-97f82095686f">EVENT_EXTENDED_ITEM_STACK_TRACE32</a> structure that contains the call stack if the event is captured on a 32-bit computer.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_STACK_TRACE64"></a><a id="event_header_ext_type_stack_trace64"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_STACK_TRACE64</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an <a href="https://msdn.microsoft.com/3c9e0dcb-1eb9-4c9f-a4c8-5a93566be303">EVENT_EXTENDED_ITEM_STACK_TRACE64</a> structure that contains the call stack if the event is captured on a 64-bit computer.

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
<td width="40%"><a id="_EVENT_HEADER_EXT_TYPE_PROV_TRAITS"></a><a id="_event_header_ext_type_prov_traits"></a><dl>
<dt><b>	EVENT_HEADER_EXT_TYPE_PROV_TRAITS</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an extended header item that  contains provider traits data, for example traits set through <a href="https://msdn.microsoft.com/e8b408ba-4bb5-4166-bf43-d18e4fe8de32">EventSetInformation(EventProviderSetTraits)</a> or specified through <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR_TYPE_PROVIDER_METADATA</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_EVENT_KEY"></a><a id="event_header_ext_type_event_key"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_EVENT_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an EVENT_EXTENDED_ITEM_EVENT_KEY structure that contains a unique event identifier which is a 64-bit scalar. 

The <b>EnableProperty</b>EVENT_ENABLE_PROPERTY_EVENT_KEY needs to be passed in for the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> call for a given provider to enable this feature.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY"></a><a id="event_header_ext_type_process_start_key"></a><dl>
<dt><b>EVENT_HEADER_EXT_TYPE_PROCESS_START_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <b>DataPtr</b> member points to an EVENT_EXTENDED_ITEM_PROCESS_START_KEY structure that contains a unique process identifier (unique across the boot session). This identifier is a 64-bit scalar. 

The <b>EnableProperty</b>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY needs to be passed in for the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> call for a given provider to enable this feature. 

</td>
</tr>
</table>
 


### -field Linkage

Reserved.


### -field DataSize

Size, in bytes, of the extended data that <b>DataPtr</b> points to.


### -field DataPtr

Pointer to the extended data. The <b>ExtType</b> member determines the type of extended data to which this member points.


#### - Reserved2

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a>
 

 

