---
UID: NF:tdh.TdhGetEventMapInformation
title: TdhGetEventMapInformation function (tdh.h)
description: Retrieves information about the event map contained in the event.
helpviewer_keywords: ["TdhGetEventMapInformation","TdhGetEventMapInformation function [ETW]","etw.tdhgeteventmapinformation_func","tdh.tdhgeteventmapinformation_func","tdh/TdhGetEventMapInformation"]
old-location: etw\tdhgeteventmapinformation_func.htm
tech.root: ETW
ms.assetid: 2625b65c-7f9e-4a87-85c6-d16857ef4987
ms.date: 12/05/2018
ms.keywords: TdhGetEventMapInformation, TdhGetEventMapInformation function [ETW], etw.tdhgeteventmapinformation_func, tdh.tdhgeteventmapinformation_func, tdh/TdhGetEventMapInformation
req.header: tdh.h
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
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhGetEventMapInformation
 - tdh/TdhGetEventMapInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhGetEventMapInformation
---

# TdhGetEventMapInformation function


## -description

Retrieves information about the event map contained in the event.

## -parameters

### -param pEvent [in]

The event record passed to your <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback. For details, see the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> structure.

### -param pMapName [in]

Null-terminated Unicode string that contains the name of the map attribute value. The name comes from the <b>MapNameOffset</b> member of the <a href="/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structure.

### -param pBuffer [out]

User-allocated buffer to receive the event map. The map could be a value map, bitmap, or pattern map. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-event_map_info">EVENT_MAP_INFO</a> structure.

### -param pBufferSize [in, out]

Size, in bytes, of the <i>pBuffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema for the event was not found or the specified map was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>resourceFileName</b> attribute in the manifest contains the location of the provider binary. When you register the manifest, the location is written to the registry. TDH was unable to find the binary based on the registered location.

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
<dt><b>ERROR_WMI_SERVER_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The WMI service is not available.

</td>
</tr>
</table>

## -remarks

You cannot use this function to retrieve event map information for WPP events.

For maps defined in a manifest, the string will contain a space at the end of the string. For example, if the value is mapped to "Monday" in the manifest, the string is returned as "Monday ".


#### Examples

For an example that shows how to call this function, see <a href="/windows/desktop/ETW/using-tdhgetproperty-to-consume-event-data">Using TdhGetProperty to Consume Event Data</a>.

<div class="code"></div>