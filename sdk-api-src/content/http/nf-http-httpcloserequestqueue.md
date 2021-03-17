---
UID: NF:http.HttpCloseRequestQueue
title: HttpCloseRequestQueue function (http.h)
description: Closes the handle to the specified request queue created by HttpCreateRequestQueue.
helpviewer_keywords: ["HttpCloseRequestQueue","HttpCloseRequestQueue function [HTTP]","http.httpcloserequestqueue","http/HttpCloseRequestQueue"]
old-location: http\httpcloserequestqueue.htm
tech.root: http
ms.assetid: dfbc2d32-c1f6-41b1-8f4f-9e5e9f6dd9e1
ms.date: 12/05/2018
ms.keywords: HttpCloseRequestQueue, HttpCloseRequestQueue function [HTTP], http.httpcloserequestqueue, http/HttpCloseRequestQueue
req.header: http.h
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpCloseRequestQueue
 - http/HttpCloseRequestQueue
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
 - HttpCloseRequestQueue
---

# HttpCloseRequestQueue function


## -description

The <b>HttpCloseRequestQueue</b> function closes the handle to the specified request queue created by <a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>.

The application must close the request queue when it is no longer required.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue that is closed. A request queue is created and its handle returned by a call to the 
<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function.

## -returns

If the function succeeds, it returns <b>NO_ERROR</b>.

If the function fails, it returns one of the following error codes.

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
The application does not have permission to close the request queue. Only the application that created the request queue can close it.

</td>
</tr>
</table>

## -remarks

Applications  should not call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> on the request queue handle; instead, they should call <b>HttpCloseRequestQueue</b> to ensure that all the resources are released.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpshutdownrequestqueue">HttpShutdownRequestQueue</a>