---
UID: NF:tdh.TdhGetProperty
title: TdhGetProperty function (tdh.h)
description: Retrieves a property value from the event data.
helpviewer_keywords: ["TdhGetProperty","TdhGetProperty function [ETW]","etw.tdhgetproperty_func","tdh.tdhgetproperty_func","tdh/TdhGetProperty"]
old-location: etw\tdhgetproperty_func.htm
tech.root: ETW
ms.assetid: 3975792e-cc24-430a-914f-420f3a5ec1d6
ms.date: 12/05/2018
ms.keywords: TdhGetProperty, TdhGetProperty function [ETW], etw.tdhgetproperty_func, tdh.tdhgetproperty_func, tdh/TdhGetProperty
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
 - TdhGetProperty
 - tdh/TdhGetProperty
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
 - TdhGetProperty
---

# TdhGetProperty function


## -description

Retrieves a property value from the event data.

## -parameters

### -param pEvent [in]

The event record passed to your <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback. For details, see the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> structure.

### -param TdhContextCount [in]

Number of elements in <i>pTdhContext</i>.

### -param pTdhContext [in]

Array of context values for WPP or classic ETW events only; otherwise, <b>NULL</b>. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-tdh_context">TDH_CONTEXT</a> structure.  The array must not contain duplicate context types.

### -param PropertyDataCount [in]

Number of data descriptor structures in <i>pPropertyData</i>.

### -param pPropertyData [in]

Array of <a href="/windows/desktop/api/tdh/ns-tdh-property_data_descriptor">PROPERTY_DATA_DESCRIPTOR</a> structures that defines the property to retrieve. 

If you called  the <a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a> function to retrieve the required buffer size for the property, you can use the same data descriptors.

If you are retrieving a property that is not a member of a structure, you can specify a single data descriptor. If you are retrieving a property that is a member of a structure, specify an array of two  data descriptors (structures cannot contain or reference other structures).

### -param BufferSize [in]

Size of the <i>pBuffer</i> buffer, in bytes. You can get this value from the <i>pPropertySize</i> parameter when calling <a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a> function.

### -param pBuffer [out]

User-allocated buffer that receives the property data.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema for the event was not found or the specified property was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The pBuffer buffer is too small. To get the required buffer size, call <a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a>.

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
<dt><b>ERROR_WMI_SERVER_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The WMI service is not available.

</td>
</tr>
</table>

## -remarks

If the event is a WPP or classic ETW event, you can specify context information that is used to help parse the event information. The event is a WPP event if the EVENT_HEADER_FLAG_TRACE_MESSAGE flag is set in the <b>Flags</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a> (see the <b>EventHeader</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a>). The event is a legacy ETW event if the EVENT_HEADER_FLAG_CLASSIC_HEADER flag is set.

For a list of properties for WPP events and their data types, see <a href="/windows/desktop/api/tdh/ns-tdh-property_data_descriptor">PROPERTY_DATA_DESCRIPTOR</a>.


#### Examples

For an example that shows how to call this function to retrieve the value of a top-level property or the member of a structure, see <a href="/windows/desktop/ETW/using-tdhgetproperty-to-consume-event-data">Using TdhGetProperty to Consume Event Data</a>.

<div class="code"></div>

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhgeteventinformation">TdhGetEventInformation</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a>