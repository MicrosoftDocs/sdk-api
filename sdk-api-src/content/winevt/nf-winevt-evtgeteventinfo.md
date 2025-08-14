---
UID: NF:winevt.EvtGetEventInfo
title: EvtGetEventInfo function (winevt.h)
description: Gets information that identifies the structured XML query that selected the event and the channel or log file that contained the event.
helpviewer_keywords: ["EvtGetEventInfo","EvtGetEventInfo function [EventLog]","wes.evtgeteventinfo","winevt/EvtGetEventInfo"]
old-location: wes\evtgeteventinfo.htm
tech.root: wes
ms.assetid: 69aa22a1-10c1-43bd-ae3b-d7641bed2065
ms.date: 12/05/2018
ms.keywords: EvtGetEventInfo, EvtGetEventInfo function [EventLog], wes.evtgeteventinfo, winevt/EvtGetEventInfo
req.header: winevt.h
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtGetEventInfo
 - winevt/EvtGetEventInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
api_name:
 - EvtGetEventInfo
---

# EvtGetEventInfo function


## -description

Gets information that identifies the structured XML query that selected the event and the channel or log file that contained the event.

## -parameters

### -param Event [in]

A handle to an event for which you want to retrieve information.

### -param PropertyId [in]

A flag that identifies the information to retrieve. For example, the query identifier or the path. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_event_property_id">EVT_EVENT_PROPERTY_ID</a> enumeration.

### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.

### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the information. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param PropertyValueBufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. Use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

</td>
</tr>
</table>

## -remarks

If the query that you passed to <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> or <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> was an XPath instead of a structured XML query, the query identifier will be zero and the path will be the path that you passed to the function.