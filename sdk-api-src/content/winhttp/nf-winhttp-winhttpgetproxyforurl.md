---
UID: NF:winhttp.WinHttpGetProxyForUrl
title: WinHttpGetProxyForUrl function (winhttp.h)
description: Retrieves the proxy data for the specified URL. (WinHttpGetProxyForUrl)
helpviewer_keywords: ["WinHttpGetProxyForUrl","WinHttpGetProxyForUrl function [WinHTTP]","http.winhttpgetproxyforurl","winhttp/WinHttpGetProxyForUrl"]
old-location: http\winhttpgetproxyforurl.htm
tech.root: http
ms.assetid: d01b101e-a496-4e84-9aec-61afe3920fbb
ms.date: 12/05/2018
ms.keywords: WinHttpGetProxyForUrl, WinHttpGetProxyForUrl function [WinHTTP], http.winhttpgetproxyforurl, winhttp/WinHttpGetProxyForUrl
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
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
 - WinHttpGetProxyForUrl
 - winhttp/WinHttpGetProxyForUrl
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
 - WinHttpGetProxyForUrl
---

# WinHttpGetProxyForUrl function


## -description

The <b>WinHttpGetProxyForUrl</b> function retrieves the proxy data for the specified URL.

## -parameters

### -param hSession [in]

The WinHTTP session handle returned by the <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a> function.

### -param lpcwszUrl [in]

A pointer to a null-terminated Unicode string that contains the URL of the HTTP request that the application is preparing to send.

### -param pAutoProxyOptions [in]

A pointer to a <a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options">WINHTTP_AUTOPROXY_OPTIONS</a> structure that specifies the auto-proxy options to use.

### -param pProxyInfo [out]

A pointer to a <a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info">WINHTTP_PROXY_INFO</a> structure that receives the proxy setting. This structure is then applied to the request handle using the WINHTTP_OPTION_PROXY option. Free the <b>lpszProxy</b> and <b>lpszProxyBypass</b> strings contained in this structure (if they are non-NULL) using the <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. For extended error data, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

  Possible error codes include the folllowing.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Returned by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl">WinHttpGetProxyForUrl</a> when a proxy for the specified URL cannot be located.

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
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

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
<dt><b>ERROR_WINHTTP_LOGIN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The login attempt failed.  When this error is encountered, close the request handle with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>.  A new request handle must be created before retrying the function that originally produced this error.

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

This function implements the Web Proxy Auto-Discovery (WPAD) protocol for automatically configuring the proxy settings for an HTTP request. The WPAD protocol downloads a Proxy Auto-Configuration (PAC) file, which is a script that identifies the proxy server to use for a given target URL. PAC files are typically deployed by the IT department within a corporate network environment. The URL of the PAC file can either be specified explicitly or <b>WinHttpGetProxyForUrl</b> can be instructed to automatically discover the location of the PAC file on the local network.

<b>WinHttpGetProxyForUrl</b> supports only ECMAScript-based PAC files.

<b>WinHttpGetProxyForUrl</b> must be called on a per-URL basis, because the PAC file can return a different proxy server for different URLs. This is useful because the PAC file enables an IT department to implement proxy server load balancing by mapping (hashing) the target URL (specified by the <i>lpcwszUrl</i> parameter) to a certain proxy in a proxy server array.

<b>WinHttpGetProxyForUrl</b> caches the autoproxy URL and the autoproxy script when auto-discovery is specified in the <b>dwFlags</b> member of the <i>pAutoProxyOptions</i> structure. For more information, see <a href="/windows/desktop/WinHttp/autoproxy-cache">Autoproxy Cache</a>.

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>
