---
UID: NF:winevt.EvtCancel
title: EvtCancel function (winevt.h)
description: Cancels all pending operations on a handle.
helpviewer_keywords: ["EvtCancel","EvtCancel function [EventLog]","wes.evtcancel","winevt/EvtCancel"]
old-location: wes\evtcancel.htm
tech.root: wes
ms.assetid: c8770139-93de-4da2-b797-f82775f4c553
ms.date: 12/05/2018
ms.keywords: EvtCancel, EvtCancel function [EventLog], wes.evtcancel, winevt/EvtCancel
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
 - EvtCancel
 - winevt/EvtCancel
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
 - EvtCancel
---

# EvtCancel function


## -description

Cancels all pending operations on a handle.

## -parameters

### -param Object

The handle whose operation you want to cancel. You can cancel the following operations:

<ul>
<li>
<a href="/windows/desktop/api/winevt/nf-winevt-evtclearlog">EvtClearLog</a>
</li>
<li>
<a href="/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a>
</li>
<li>
<a href="/windows/desktop/api/winevt/nf-winevt-evtnext">EvtNext</a>
</li>
<li>
<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>
</li>
<li>
<a href="/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a>
</li>
<li>
<a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a>
</li>
</ul>
To cancel the <a href="/windows/desktop/api/winevt/nf-winevt-evtclearlog">EvtClearLog</a>, 
       <a href="/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a>, 
       <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>, and 
       <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> operations, you must pass the session 
       handle. To specify the default session (local session), set this parameter to 
       <b>NULL</b>.

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
The function failed. To get the error code, call the 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

Use this function to cancel long-running operations. For example, calling the 
    <a href="/windows/desktop/api/winevt/nf-winevt-evtnext">EvtNext</a> function could theoretically take a long time due to 
    the filtering of thousands of event records.  Calling 
    <b>EvtCancel</b> would stop the 
    <b>EvtNext</b> function from processing further event records. Note 
    that the function may not be able to stop the operation immediately.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the handle 
    when done.

The following procedure describes how to cancel a long-running operation.

<p class="proch"><b>To cancel a long-running operation</b>

<ol>
<li>Thread A calls a long running operation (for example,  the 
      <a href="/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a> function).</li>
<li>Thread B wants to cancel and close all operations, so thread B calls the 
      <b>EvtCancel</b> function.</li>
<li>Thread B then waits for all pending calls to complete (by synchronizing with thread A). Because the 
      <b>EvtCancel</b> function was called, thread A should complete 
      soon after the call to the <b>EvtCancel</b> was made.</li>
<li>After thread A has fully completed the operation 
      (<a href="/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a>), thread B can close the query result handle using 
      the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function.</li>
</ol>
The operation being stopped will return with an error code of ERROR_CANCELLED.