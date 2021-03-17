---
UID: NF:http.HttpWaitForDisconnect
title: HttpWaitForDisconnect function (http.h)
description: Notifies the application when the connection to an HTTP client is broken for any reason.
helpviewer_keywords: ["HttpWaitForDisconnect","HttpWaitForDisconnect function [HTTP]","_http_httpwaitfordisconnect","http.httpwaitfordisconnect","http/HttpWaitForDisconnect"]
old-location: http\httpwaitfordisconnect.htm
tech.root: http
ms.assetid: 1f1c16c1-43ef-4e29-8d3d-8592ce6a6bf0
ms.date: 12/05/2018
ms.keywords: HttpWaitForDisconnect, HttpWaitForDisconnect function [HTTP], _http_httpwaitfordisconnect, http.httpwaitfordisconnect, http/HttpWaitForDisconnect
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpWaitForDisconnect
 - http/HttpWaitForDisconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpWaitForDisconnect
---

# HttpWaitForDisconnect function


## -description

The 
<b>HttpWaitForDisconnect</b> function notifies the application when the connection to an HTTP client is broken for any reason.

## -parameters

### -param RequestQueueHandle [in]

A handle to the request queue that handles requests from the specified connection. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

### -param ConnectionId [in]

Identifier for the connection to the client computer. This value is returned in the <b>ConnectionID</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a> function.

### -param Overlapped [in]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the connection is broken, whereas an asynchronous call immediately returns ERROR_IO_PENDING and the calling application then uses 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For information about using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structures for synchronization, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function is used asynchronously, a return value of ERROR_IO_PENDING indicates that the next request is not yet ready and is retrieved later through normal overlapped I/O completion mechanisms.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied parameters is in an unusable form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>