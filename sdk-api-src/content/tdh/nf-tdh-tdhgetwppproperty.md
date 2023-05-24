---
UID: NF:tdh.TdhGetWppProperty
title: TdhGetWppProperty function (tdh.h)
description: Retrieves a specific property associated with a WPP message.
helpviewer_keywords: ["TdhGetWppProperty","TdhGetWppProperty function [ETW]","etw.tdhgetwppproperty","tdh/TdhGetWppProperty"]
old-location: etw\tdhgetwppproperty.htm
tech.root: ETW
ms.assetid: a9c5ed0f-af6f-4500-9ef7-bc60b8911ea0
ms.date: 12/05/2018
ms.keywords: TdhGetWppProperty, TdhGetWppProperty function [ETW], etw.tdhgetwppproperty, tdh/TdhGetWppProperty
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - TdhGetWppProperty
 - tdh/TdhGetWppProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhGetWppProperty
---

# TdhGetWppProperty function


## -description

Retrieves a specific property associated with a WPP message.

## -parameters

### -param Handle [in]

Type: <b>TDH_HANDLE</b>

A valid decoding handle.

### -param EventRecord [in]

Type: <b><a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">PEVENT_RECORD</a></b>

The event record passed to your <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback.

### -param PropertyName [in]

Type: <b>PWSTR</b>

The name of the property to retrieve.

For a list of  possible values, see <a href="/windows/desktop/api/tdh/ns-tdh-property_data_descriptor">PROPERTY_DATA_DESCRIPTOR</a>.

### -param BufferSize [in, out]

Type: <b>PULONG</b>

Size of the <i>Buffer</i> parameter, in bytes.

### -param Buffer [out]

Type: <b>PBYTE</b>

User-allocated buffer that receives the property data.

## -returns

Type: <b>ULONG</b>

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
The specified property was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>BufferSize</i> is too small. To get the required buffer size, call <a href="/windows/desktop/api/tdh/nf-tdh-tdhgetwppproperty">TdhGetWppProperty</a> twice, once with a null buffer and a pointer to retrieve the buffer size and then again with the correctly sized buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is incorrect. This error is returned if the <i>Handle</i>, <i>EventRecord</i>, <i>PropertyName</i>, or <i>Buffer</i>    parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To retrieve only the decoded event message without specifying a property name, call <a href="/windows/desktop/api/tdh/nf-tdh-tdhgetwppmessage">TdhGetWppMessage</a>.

## -see-also
<a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a>



<a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetwppmessage">TdhGetWppMessage</a>