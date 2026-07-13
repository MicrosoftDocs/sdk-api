---
UID: NF:wininet.InternetOpenW
title: InternetOpenW function (wininet.h)
description: Initializes an application's use of the WinINet functions. (Unicode)
helpviewer_keywords: ["InternetOpen", "InternetOpen function [WinINet]", "InternetOpenW", "_inet_internetopen_function", "wininet.internetopen", "wininet/InternetOpen", "wininet/InternetOpenW"]
old-location: wininet\internetopen.htm
tech.root: wininet
ms.assetid: 9ec087c9-d484-4763-a527-2ea5c1a0cf28
ms.date: 12/05/2018
ms.keywords: InternetOpen, InternetOpen function [WinINet], InternetOpenA, InternetOpenW, _inet_internetopen_function, wininet.internetopen, wininet/InternetOpen, wininet/InternetOpenA, wininet/InternetOpenW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetOpenW (Unicode) and InternetOpenA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetOpenW
 - wininet/InternetOpenW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetOpen
 - InternetOpenA
 - InternetOpenW
---

# InternetOpenW function


## -description

Initializes an application's use of the WinINet functions.

## -parameters

### -param lpszAgent [in]

Pointer to a <b>null</b>-terminated string  that specifies the name of the application or entity calling the WinINet functions. This name is used as the user agent in the HTTP protocol.

### -param dwAccessType [in]

Type of access required. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_OPEN_TYPE_DIRECT</dt>
</dl>
</td>
<td width="60%">
Resolves all host names locally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_OPEN_TYPE_PRECONFIG</dt>
</dl>
</td>
<td width="60%">
Retrieves the proxy or direct configuration from the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_OPEN_TYPE_PRECONFIG_WITH_NO_AUTOPROXY</dt>
</dl>
</td>
<td width="60%">
Retrieves the proxy or direct configuration from the registry and prevents the use of a startup Microsoft JScript or Internet Setup (INS) file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_OPEN_TYPE_PROXY</dt>
</dl>
</td>
<td width="60%">
Passes requests to the proxy unless a proxy bypass list is supplied and the name to be resolved bypasses the proxy. In this case, the function uses 
<b>INTERNET_OPEN_TYPE_DIRECT</b>.

</td>
</tr>
</table>

### -param lpszProxy [in]

Pointer to a <b>null</b>-terminated string  that specifies the name of the proxy server(s) to use when proxy access is specified by setting 
<i>dwAccessType</i> to 
<b>INTERNET_OPEN_TYPE_PROXY</b>. Do not use an empty string, because 
<b>InternetOpen</b> will use it as the proxy name. The WinINet functions recognize only CERN type proxies (HTTP only) and the TIS FTP gateway (FTP only). If Microsoft Internet Explorer is installed, these functions also support SOCKS proxies. FTP requests can be made through a CERN type proxy either by changing them to an HTTP request or by using 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a>. If 
<i>dwAccessType</i> is not set to 
<b>INTERNET_OPEN_TYPE_PROXY</b>, this parameter is ignored and should be <b>NULL</b>. For more information about listing proxy servers, see the 
<a href="/windows/desktop/WinInet/enabling-internet-functionality">Listing Proxy Servers</a> section of 
<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>.

### -param lpszProxyBypass [in]

Pointer to a <b>null</b>-terminated string  that specifies an optional list of host names or IP addresses, or both, that should not be routed through the proxy when 
<i>dwAccessType</i> is set to 
<b>INTERNET_OPEN_TYPE_PROXY</b>. The list can contain wildcards. Do not use an empty string, because 
<b>InternetOpen</b> will use it as the proxy bypass list. If this parameter specifies the "&lt;local&gt;" macro, the function bypasses the proxy for any host name that does not contain a period. 

By default, WinINet will bypass the proxy for requests that use the host names "localhost", "loopback", "127.0.0.1", or "[::1]". This behavior exists because a remote proxy server typically will not resolve these addresses properly.<b>Internet Explorer 9:  </b>You can remove the local computer from the proxy bypass list using the "&lt;-loopback&gt;" macro.



If 
<i>dwAccessType</i> is not set to 
<b>INTERNET_OPEN_TYPE_PROXY</b>, this parameter is ignored and should be <b>NULL</b>.

### -param dwFlags [in]

Options. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_ASYNC</dt>
</dl>
</td>
<td width="60%">
Makes only asynchronous requests on handles descended from the handle returned from this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_FROM_CACHE</dt>
</dl>
</td>
<td width="60%">
Does not make network requests. All entities are returned from the cache. If the requested item is not in the cache, a suitable error, such as ERROR_FILE_NOT_FOUND, is returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_OFFLINE</dt>
</dl>
</td>
<td width="60%">
Identical to 
<b>INTERNET_FLAG_FROM_CACHE</b>. Does not make network requests. All entities are returned from the cache. If the requested item is not in the cache, a suitable error, such as ERROR_FILE_NOT_FOUND, is returned.

</td>
</tr>
</table>

## -returns

Returns a valid handle that the application passes to subsequent WinINet functions. If 
<b>InternetOpen</b> fails, it returns <b>NULL</b>. To retrieve a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>InternetOpen</b> is the first WinINet function called by an application. It tells the Internet DLL to initialize internal data structures and prepare for future calls from the application. When the application finishes using the Internet functions, it should call 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> to free the handle and any associated resources.

The application can make any number of calls to 
<b>InternetOpen</b>, though a single call is normally sufficient. The application might need to define separate behaviors for each 
<b>InternetOpen</b> instance, such as different proxy servers configured for each.

After the calling application has finished using the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle returned by 
<b>InternetOpen</b>, it must be closed using the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> function.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetOpen as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
