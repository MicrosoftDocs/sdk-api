---
UID: NF:winevt.EvtNext
title: EvtNext function (winevt.h)
description: Gets the next event from the query or subscription results.
helpviewer_keywords: ["EvtNext","EvtNext function [EventLog]","wes.evtnext","winevt/EvtNext"]
old-location: wes\evtnext.htm
tech.root: wes
ms.assetid: 46d40734-f022-4775-aa4f-13f4069c43c8
ms.date: 12/05/2018
ms.keywords: EvtNext, EvtNext function [EventLog], wes.evtnext, winevt/EvtNext
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
 - EvtNext
 - winevt/EvtNext
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
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtNext
---

# EvtNext function


## -description

Gets the next event from the query or subscription results.

## -parameters

### -param ResultSet [in]

The handle to a query or subscription result set that the <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> function or the <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> function returns.

### -param EventsSize [in]

The number of elements in the <i>EventArray</i> array. The function will try to retrieve this number of elements from the result set.

### -param Events [in]

A pointer to an array of handles that will be set to the handles to the events from the result set.

### -param Timeout [in]

The number of milliseconds that you are willing to wait for a result.  Set to INFINITE to indicate no time-out value. If the time-out expires, the last error is set to ERROR_TIMEOUT.

### -param Flags [in]

Reserved. Must be zero.

### -param Returned [out]

The number of handles in the array that are set.

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

Call this function in a loop until the function returns <b>FALSE</b> and the error code is ERROR_NO_MORE_ITEMS.

For each event that you retrieve, you can then call the <a href="/windows/desktop/api/winevt/nf-winevt-evtcreaterendercontext">EvtCreateRenderContext</a> and <a href="/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a> functions to render the event.

You must call <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> on each event handle that you receive.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/querying-for-events">Querying for Events</a> and <a href="/windows/desktop/WES/subscribing-to-events">Subscribing to Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a>