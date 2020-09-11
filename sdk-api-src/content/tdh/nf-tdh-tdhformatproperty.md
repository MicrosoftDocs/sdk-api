---
UID: NF:tdh.TdhFormatProperty
title: TdhFormatProperty function (tdh.h)
description: Formats a property value for display.
helpviewer_keywords: ["TdhFormatProperty","TdhFormatProperty function [ETW]","etw.tdhformatproperty","tdh/TdhFormatProperty"]
old-location: etw\tdhformatproperty.htm
tech.root: ETW
ms.assetid: ecc954f8-840e-4963-a0c8-64aac25355e3
ms.date: 12/05/2018
ms.keywords: TdhFormatProperty, TdhFormatProperty function [ETW], etw.tdhformatproperty, tdh/TdhFormatProperty
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhFormatProperty
 - tdh/TdhFormatProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhFormatProperty
---

# TdhFormatProperty function


## -description

Formats a property value for display.

## -parameters

### -param EventInfo [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-trace_event_info">TRACE_EVENT_INFO</a> structure that contains the event information. To get this structure, call the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhgeteventinformation">TdhGetEventInformation</a> function.

### -param MapInfo [in, optional]

An <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_map_info">EVENT_MAP_INFO</a> structure that maps integer and bit values to strings. To get this structure, call the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhgeteventmapinformation">TdhGetEventMapInformation</a> function. To get the name of the map, use the <b>MapNameOffset</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structure. If you do not provide the map information for a mapped property, the function formats the integer or bit value.

### -param PointerSize [in]

The size of a pointer value in the event data. To get the size, access the <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_RECORD.EventHeader.Flags</a> member. The pointer size is 4 bytes if the EVENT_HEADER_FLAG_32_BIT_HEADER flag is set; otherwise, it is 8 bytes if the EVENT_HEADER_FLAG_64_BIT_HEADER flag is set. The <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> structure is passed to your <a href="https://docs.microsoft.com/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback function.

### -param PropertyInType [in]

The input type of the property. Use the <b>InType</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structure to set this parameter.

### -param PropertyOutType [in]

The output type of the property. Use the <b>OutType</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structure to set this parameter.

### -param PropertyLength [in]

The length, in bytes, of the property. Use the <b>Length</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structure to set this parameter.

### -param UserDataLength [in]

The size, in bytes, of the <i>UserData</i> buffer. See Remarks.

### -param UserData [in]

The buffer that contains the event data. See Remarks.

### -param BufferSize [in, out]

The size, in bytes, of the <i>Buffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

### -param Buffer [out, optional]

A caller-allocated buffer that contains the formatted property value. To determine the required buffer size, set this parameterto <b>NULL</b> and <i>BufferSize</i> to zero.

### -param UserDataConsumed [out]

The length, in bytes, of the consumed event data. Use this value to adjust the values of the <i>UserData</i> and <i>UserDataLength</i> parameters. See Remarks.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>pBuffer</i> buffer is too small. Use the required buffer size set in <i>pBufferSize</i> to allocate a new buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EVT_INVALID_EVENT_DATA</b></dt>
</dl>
</td>
<td width="60%">
The event data does not match the event definition in the manifest.

</td>
</tr>
</table>

## -remarks

Typically, you call this function in a loop.  Use the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-trace_event_info">TRACE_EVENT_INFO.TopLevelPropertyCount</a> member to control the loop (the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhgeteventinformation">TdhGetEventInformation</a> function returns the  <b>TRACE_EVENT_INFO</b> structure). Before entering the loop, you set the <i>UserData</i> and <i>UserDataLength</i> parameters to the value of the <b>UserData</b> and <b>UserDataLength</b> members of the <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> structure, respectively. The <b>EVENT_RECORD</b> structure is passed to your <a href="https://docs.microsoft.com/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback function. 

Determine whether the property is an array. The property is an array if the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO.Flags</a> member is set to PropertyParamCount or the <b>EVENT_PROPERTY_INFO.count</b> member is greater than 1. Call the <b>TdhFormatProperty</b> function in a loop based on the number of elements in the array.

After calling the <b>TdhFormatProperty</b> function, use the <i>UserDataConsumed</i> parameter value to set the new values of the <i>UserData</i> and <i>UserDataLength</i> parameters (Subtract <i>UserDataConsumed</i> from <i>UserDataLength</i> and use <i>UserDataLength</i> to increment the <i>UserData</i> pointer).

If the property is an IP V6 address, you must set the <i>PropertyLength</i> parameter to the size of the <b>IN6_ADDR</b> structure. The property is considered an IP V6 address if the following conditions are met:

<ul>
<li>The <b>InType</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> is TDH_INTYPE_BINARY</li>
<li>The <b>OutType</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> is TDH_OUTTYPE_IPV6</li>
<li>The <b>Length</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> is 0</li>
</ul>

#### Examples

For an example that shows how to call this function , see <a href="https://docs.microsoft.com/windows/desktop/ETW/using-tdhformatproperty-to-consume-event-data">Using TdhFormatProperty to Consume Event Data</a>.

<div class="code"></div>

