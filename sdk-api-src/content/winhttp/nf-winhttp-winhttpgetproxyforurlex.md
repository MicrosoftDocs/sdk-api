---
UID: NF:winhttp.WinHttpGetProxyForUrlEx
title: WinHttpGetProxyForUrlEx function (winhttp.h)
description: Retrieves the proxy data for the specified URL. (WinHttpGetProxyForUrlEx)
helpviewer_keywords: ["WinHttpGetProxyForUrlEx","WinHttpGetProxyForUrlEx function [WinHTTP]","http.winhttpgetproxyforurlex","winhttp/WinHttpGetProxyForUrlEx"]
old-location: http\winhttpgetproxyforurlex.htm
tech.root: http
ms.assetid: 28479a55-7a25-4254-b27a-45e09b166dd5
ms.date: 12/05/2018
ms.keywords: WinHttpGetProxyForUrlEx, WinHttpGetProxyForUrlEx function [WinHTTP], http.winhttpgetproxyforurlex, winhttp/WinHttpGetProxyForUrlEx
req.header: winhttp.h
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpGetProxyForUrlEx
 - winhttp/WinHttpGetProxyForUrlEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpGetProxyForUrlEx
---

# WinHttpGetProxyForUrlEx function


## -description

The  <b>WinHttpGetProxyForUrlEx</b> function retrieves the proxy data for the specified URL.

## -parameters

### -param hResolver [in]

The WinHTTP resolver handle returned by the <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcreateproxyresolver">WinHttpCreateProxyResolver</a> function.

### -param pcwszUrl [in]

A pointer to a null-terminated Unicode string that contains a URL for which proxy information will be determined.

### -param pAutoProxyOptions [in]

A pointer to a <a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options">WINHTTP_AUTOPROXY_OPTIONS</a> structure that specifies the auto-proxy options to use.

### -param pContext [in]

Context data that will be passed to the completion callback function.

## -returns

A status code indicating the result of the operation.

<table>
<tr>
<th>The following codes may be returned.</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is continuing asynchronously.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Returned by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a> when a proxy for the specified URL cannot be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT</b></dt>
</dl>
</td>
<td width="60%">
An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INVALID_URL</b></dt>
</dl>
</td>
<td width="60%">
The URL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_OPERATION_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT</b></dt>
</dl>
</td>
<td width="60%">
The PAC file could not be downloaded. For example, the server referenced by the PAC URL may not have been reachable, or  the server returned a 404 NOT FOUND response.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_UNRECOGNIZED_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
The URL of the PAC file specified a scheme other than "http:" or "https:".

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

This function implements the Web Proxy Auto-Discovery (WPAD) protocol for automatically configuring the proxy settings for an HTTP request. The WPAD protocol downloads a Proxy Auto-Configuration (PAC) file, which is a script that identifies the proxy server to use for a given target URL. PAC files are typically deployed by the IT department within a corporate network environment. The URL of the PAC file can either be specified explicitly or <b>WinHttpGetProxyForUrlEx</b> can be instructed to automatically discover the location of the PAC file on the local network.

<b>WinHttpGetProxyForUrlEx</b> supports only ECMAScript-based PAC files.

<b>WinHttpGetProxyForUrlEx</b> must be called on a per-URL basis, because the PAC file can return a different proxy server for different URLs. This is useful because the PAC file enables an IT department to implement proxy server load balancing by mapping (hashing) the target URL (specified by the <i>lpcwszUrl</i> parameter) to a certain proxy in a proxy server array.

<b>WinHttpGetProxyForUrlEx</b> caches the autoproxy URL and the autoproxy script when auto-discovery is specified in the <b>dwFlags</b> member of the <i>pAutoProxyOptions</i> structure. For more information, see <a href="/windows/desktop/WinHttp/autoproxy-cache">Autoproxy Cache</a>.

<b>WinHttpGetProxyForUrlEx</b> provides a fully Asynchronous and cancellable API that <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl">WinHttpGetProxyForUrl</a> does not.  <b>WinHttpGetProxyForUrlEx</b> also provides the application with the full proxy list that was returned by the PAC script allowing the application to better handle failover to "DIRECT" and to understand SOCKS if desired.

<b>WinHttpGetProxyForUrlEx</b> always executes asynchronously and returns immediately with <b>ERROR_IO_PENDING</b> on success. The callback is set by calling <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a> on the <i>hSession</i> provided by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>.  Alternately call <b>WinHttpSetStatusCallback</b> on the <i>hResolver</i> provided by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcreateproxyresolver">WinHttpCreateProxyResolver</a> to have a specific callback for each call. 

You must call <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a> before <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpcreateproxyresolver">WinHttpCreateProxyResolver</a>. When calling <b>WinHttpSetStatusCallback</b>, use <b>WINHTTP_CALLBACK_FLAG_REQUEST_ERROR |
                                              WINHTTP_CALLBACK_FLAG_GETPROXYFORURL_COMPLETE</b>. See <a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a> for information on the use of the callback.

Once a callback of status <b>WINHTTP_CALLBACK_STATUS_GETPROXYFORURL_COMPLETE</b> is returned, the application can call <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyresult">WinHttpGetProxyResult</a> on the resolver handle used to issue <b>WinHttpGetProxyForUrlEx</b> to receive the results of that call.


If the call fails after returning <b>ERROR_IO_PENDING</b> then a callback of <b>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</b> will be issued.

This function always executes out-of-process.
