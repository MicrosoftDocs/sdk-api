---
UID: NF:winevt.EvtGetQueryInfo
title: EvtGetQueryInfo function (winevt.h)
description: Gets information about a query that you ran that identifies the list of channels or log files that the query attempted to access. The function also gets a list of return codes that indicates the success or failure of each access.
helpviewer_keywords: ["EvtGetQueryInfo","EvtGetQueryInfo function [EventLog]","wes.evtgetqueryinfo","winevt/EvtGetQueryInfo"]
old-location: wes\evtgetqueryinfo.htm
tech.root: wes
ms.assetid: 311a2060-90d9-41ec-b489-c07d3e813187
ms.date: 12/05/2018
ms.keywords: EvtGetQueryInfo, EvtGetQueryInfo function [EventLog], wes.evtgetqueryinfo, winevt/EvtGetQueryInfo
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
 - EvtGetQueryInfo
 - winevt/EvtGetQueryInfo
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
 - EvtGetQueryInfo
---

# EvtGetQueryInfo function


## -description

Gets information about a query that you ran that identifies the list of channels or log files that the query attempted to access. The function also gets a list of return codes that indicates the success or failure of each access.

## -parameters

### -param QueryOrSubscription [in]

 A handle to the query that the<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> or  <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> function returns.

### -param PropertyId [in]

The identifier of the query information to retrieve. For a list of identifiers, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_query_property_id">EVT_QUERY_PROPERTY_ID</a> enumeration.

### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.

### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the query information. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

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
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

You only need to call this function, if you pass the EvtQueryTolerateQueryErrors flag to <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> or the EvtSubscribeTolerateQueryErrors flag to <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a>.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/querying-for-events">Querying for Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a>