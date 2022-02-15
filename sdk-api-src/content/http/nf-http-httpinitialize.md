---
UID: NF:http.HttpInitialize
title: HttpInitialize function (http.h)
description: The HttpInitialize function initializes the HTTP Server API driver, starts it, if it has not already been started, and allocates data structures for the calling application to support response-queue creation and other operations.
helpviewer_keywords: ["HTTP_INITIALIZE_CONFIG","HTTP_INITIALIZE_SERVER","HttpInitialize","HttpInitialize function [HTTP]","_http_httpinitialize","http.httpinitialize","http/HttpInitialize"]
old-location: http\httpinitialize.htm
tech.root: http
ms.assetid: bc0648a9-bacf-4b09-aa4e-66aecbbdca3d
ms.date: 12/05/2018
ms.keywords: HTTP_INITIALIZE_CONFIG, HTTP_INITIALIZE_SERVER, HttpInitialize, HttpInitialize function [HTTP], _http_httpinitialize, http.httpinitialize, http/HttpInitialize
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
 - HttpInitialize
 - http/HttpInitialize
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
 - HttpInitialize
---

# HttpInitialize function

## -description

The <b>HttpInitialize</b> function initializes the HTTP Server API driver, starts it, if it has not already been started, and allocates data structures for the calling application to support response-queue creation and other operations. Call this function before calling any other functions in the HTTP Server API.

## -parameters

### -param Version [in]

HTTP version. This parameter is an 
<a href="/windows/win32/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure. For the current version, declare an instance of the structure and set it to the pre-defined value **HTTPAPI_VERSION_1** before passing it to 
<b>HttpInitialize</b>.

### -param Flags [in]

Initialization options, which can include one or both of the following values.

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
Perform initialization for applications that use the HTTP configuration functions, 
<a href="/windows/win32/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>, 
<a href="/windows/win32/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>, 
<a href="/windows/win32/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>, and 
<a href="/windows/win32/api/http/nf-http-httpisfeaturesupported">HttpIsFeatureSupported</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_INITIALIZE_SERVER"></a><a id="http_initialize_server"></a><dl>
<dt><b>HTTP_INITIALIZE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Perform initialization for applications that use the HTTP Server API.

</td>
</tr>
</table>

### -param pReserved [in, out]

This parameter is reserved, and must be <b>NULL</b>.

## -returns

If the function succeeds, then the return value is **NO_ERROR**.

If the function fails, then the return value is one of the following error codes.

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
The <i>Flags</i> parameter contains an unsupported value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/win32/debug/system-error-codes">system error code</a> defined in WinError.h.

</td>
</tr>
</table>

## -remarks

Call 
<a href="/windows/win32/api/http/nf-http-httpterminate">HttpTerminate</a> when the application completes. All the same flags that were passed to 
<b>HttpInitialize</b> in the <i>Flags</i> parameter must also be passed to 
<b>HttpTerminate</b>. An application can call 
<b>HttpInitialize</b> repeatedly, provided that each call to 
<b>HttpInitialize</b> is later matched by a corresponding call to 
<b>HttpTerminate</b>.

## -see-also

* <a href="/windows/win32/http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>
* <a href="/windows/win32/api/http/nf-http-httpterminate">HttpTerminate</a>
