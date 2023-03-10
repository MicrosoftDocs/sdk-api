---
UID: NF:http.HttpTerminate
title: HttpTerminate function (http.h)
description: Cleans up resources used by the HTTP Server API to process calls by an application.
helpviewer_keywords: ["HTTP_INITIALIZE_CONFIG","HTTP_INITIALIZE_SERVER","HttpTerminate","HttpTerminate function [HTTP]","_http_httpterminate","http.httpterminate","http/HttpTerminate"]
old-location: http\httpterminate.htm
tech.root: http
ms.assetid: d1922375-3d59-45a7-9d1d-08dbce1111ff
ms.date: 12/05/2018
ms.keywords: HTTP_INITIALIZE_CONFIG, HTTP_INITIALIZE_SERVER, HttpTerminate, HttpTerminate function [HTTP], _http_httpterminate, http.httpterminate, http/HttpTerminate
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
 - HttpTerminate
 - http/HttpTerminate
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
 - HttpTerminate
---

# HttpTerminate function


## -description

The 
<b>HttpTerminate</b> function cleans up resources used by the HTTP Server API to process calls by an application. An application should call 
<b>HttpTerminate</b> once for every time it called 
<a href="/windows/desktop/api/http/nf-http-httpinitialize">HttpInitialize</a>, with matching flag settings.

## -parameters

### -param Flags [in]

Termination options. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_INITIALIZE_CONFIG"></a><a id="http_initialize_config"></a><dl>
<dt><b>HTTP_INITIALIZE_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
Release all resources used by applications that modify the HTTP configuration.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_INITIALIZE_SERVER"></a><a id="http_initialize_server"></a><dl>
<dt><b>HTTP_INITIALIZE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Release all resources used by server applications.

</td>
</tr>
</table>

### -param pReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is NO_ERROR.

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

## -remarks

Every call to 
<a href="/windows/desktop/api/http/nf-http-httpinitialize">HttpInitialize</a> should be matched by a corresponding call to 
<b>HttpTerminate</b>. For example, if you call 
<b>HttpInitialize</b> with HTTP_INITIALIZE_SERVER, you must call 
<b>HttpTerminate</b> with HTTP_INITIALIZE_SERVER. If you call 
<b>HttpInitialize</b> twice, once with HTTP_INITIALIZE_SERVER and the second time with HTTP_INITIALIZE_CONFIG, you can call 
<b>HttpTerminate</b> one time with both flags.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpinitialize">HttpInitialize</a>