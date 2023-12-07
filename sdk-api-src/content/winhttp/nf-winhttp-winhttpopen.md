---
UID: NF:winhttp.WinHttpOpen
title: WinHttpOpen function (winhttp.h)
description: Initializes, for an application, the use of WinHTTP functions and returns a WinHTTP-session handle.
helpviewer_keywords: ["WINHTTP_ACCESS_TYPE_AUTOMATIC_PROXY","WINHTTP_ACCESS_TYPE_DEFAULT_PROXY","WINHTTP_ACCESS_TYPE_NAMED_PROXY","WINHTTP_ACCESS_TYPE_NO_PROXY","WINHTTP_FLAG_ASYNC","WinHttpOpen","WinHttpOpen function [WinHTTP]","http.winhttpopen","winhttp.winhttpopen_function","winhttp/WinHttpOpen"]
old-location: http\winhttpopen.htm
tech.root: http
ms.assetid: 34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33
ms.date: 12/05/2018
ms.keywords: WINHTTP_ACCESS_TYPE_AUTOMATIC_PROXY, WINHTTP_ACCESS_TYPE_DEFAULT_PROXY, WINHTTP_ACCESS_TYPE_NAMED_PROXY, WINHTTP_ACCESS_TYPE_NO_PROXY, WINHTTP_FLAG_ASYNC, WinHttpOpen, WinHttpOpen function [WinHTTP], http.winhttpopen, winhttp.winhttpopen_function, winhttp/WinHttpOpen
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
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpOpen
 - winhttp/WinHttpOpen
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
 - WinHttpOpen
---

# WinHttpOpen function


## -description

The <b>WinHttpOpen</b> function initializes, for an application, the use of WinHTTP functions and returns a WinHTTP-session handle.

## -parameters

### -param pszAgentW [in, optional]

A pointer to a string variable that contains the name of the application or entity calling the WinHTTP functions. This name is used as the <a href="/windows/desktop/WinHttp/glossary">user agent</a> in the HTTP protocol.

### -param dwAccessType [in]

Type of access required. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_NO_PROXY"></a><a id="winhttp_access_type_no_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_NO_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Resolves all host names directly without a proxy.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_DEFAULT_PROXY"></a><a id="winhttp_access_type_default_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Important</b>  Use of this option is deprecated on Windows 8.1 and newer. Use WINHTTP_ACCESS_TYPE_AUTOMATIC_PROXY instead.</div>
<div> </div>
Retrieves the static proxy or direct configuration from the registry. <b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b> does not inherit browser proxy settings.

The WinHTTP proxy configuration is set by one of these mechanisms.<ul>
<li>The <a href="/windows/win32/winhttp/netsh-exe-commands">Netsh.exe commands</a> on Windows Vista and Windows Server 2008 or later.</li>
<li>The <a href="/windows/desktop/WinHttp/proxycfg-exe--a-proxy-configuration-tool">proxycfg.exe</a> utility on Windows XP and Windows Server 2003 or earlier.</li>
<li>
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration">WinHttpSetDefaultProxyConfiguration</a> on all platforms.</li>
</ul>


</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_NAMED_PROXY"></a><a id="winhttp_access_type_named_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Passes requests to the proxy unless a proxy bypass list is supplied and the name to be resolved bypasses the proxy. In this case, this function uses 
the values passed for <i>pwszProxyName</i> and <i>pwszProxyBypass</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ACCESS_TYPE_AUTOMATIC_PROXY"></a><a id="winhttp_access_type_automatic_proxy"></a><dl>
<dt><b>WINHTTP_ACCESS_TYPE_AUTOMATIC_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Uses system and per-user proxy settings (including the Internet Explorer proxy configuration) to determine which proxy/proxies to use. Automatically attempts to handle failover between multiple proxies, different proxy configurations per interface, and authentication. Supported in Windows 8.1 and newer.

</td>
</tr>
</table>

### -param pszProxyW [in]

A pointer to a string variable that contains the name of the proxy server to use when proxy access is specified by setting 
<i>dwAccessType</i> to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>. The WinHTTP functions recognize only CERN type proxies for HTTP. If 
<i>dwAccessType</i> is not set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>, this parameter must be set to <b>WINHTTP_NO_PROXY_NAME</b>.

### -param pszProxyBypassW [in]

A pointer to a string variable that contains an optional semicolon delimited list of host names or IP addresses, or both, that should not be routed through the proxy when 
<i>dwAccessType</i> is set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>. The list can contain wildcard characters. Do not use an empty string, because the 
<b>WinHttpOpen</b> function uses it as the proxy bypass list. If this parameter specifies the "&lt;local&gt;" macro in the list as the only entry, this function bypasses any host name that does not contain a period. If 
<i>dwAccessType</i> is not set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>, this parameter must be set to <b>WINHTTP_NO_PROXY_BYPASS</b>.

### -param dwFlags [in]

Unsigned long integer value that contains the flags that indicate various options affecting the behavior of this function. This parameter can have the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_ASYNC"></a><a id="winhttp_flag_async"></a><dl>
<dt><b>WINHTTP_FLAG_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
Use the WinHTTP functions asynchronously. By default, all WinHTTP functions that use the returned 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle are performed synchronously. When this flag is set, the caller needs to specify a callback function through <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_SECURE_DEFAULTS"></a><a id="winhttp_flag_secure_defaults"></a><dl>
<dt><b>WINHTTP_FLAG_SECURE_DEFAULTS</b></dt>
</dl>
</td>
<td width="60%">
When this flag is set, WinHttp will require use of TLS 1.2 or newer. If the caller attempts to enable older TLS versions by setting <b>WINHTTP_OPTION_SECURE_PROTOCOLS</b>, it will fail with <b>ERROR_ACCESS_DENIED</b>. Additionally, TLS fallback will be disabled. Note that setting this flag also sets flag <b>WINHTTP_FLAG_ASYNC</b>.

</td>
</tr>
</table>

## -returns

Returns a valid session handle if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

We strongly recommend that you use WinHTTP in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <b>WinHttpOpen</b>, so that usage of the returned <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> become asynchronous). The return value indicates success or failure. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The 
<b>WinHttpOpen</b> function is the first of the WinHTTP functions called by an application. It initializes internal WinHTTP data structures and prepares for future calls from the application. When the application finishes using the WinHTTP functions, it must call 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a> to free the session handle and any associated resources.

The application can make any number of calls to 
<b>WinHttpOpen</b>, though a single call is normally sufficient. Each call to 
<b>WinHttpOpen</b> opens a new session context. Because user data is not shared between multiple session contexts, an application that makes requests on behalf of multiple users should create a separate session for each user, so as not to share user-specific cookies and authentication state. The application should define separate behaviors for each 
<b>WinHttpOpen</b> instance, such as different proxy servers configured for each.

After the calling application has finished using the 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<b>WinHttpOpen</b>, it must be closed using the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a> function.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a>.</div>
<div> </div>

#### Examples

The following example code shows how to retrieve the default connection time-out value.


```cpp

    DWORD data;
    DWORD dwSize = sizeof(DWORD);

    // Use WinHttpOpen to obtain an HINTERNET handle.
    HINTERNET hSession = WinHttpOpen(L"A WinHTTP Example Program/1.0", 
                                    WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                                    WINHTTP_NO_PROXY_NAME, 
                                    WINHTTP_NO_PROXY_BYPASS, 0);
    if (hSession)
    {


        // Use WinHttpQueryOption to retrieve internet options.
        if (WinHttpQueryOption( hSession, 
                                WINHTTP_OPTION_CONNECT_TIMEOUT, 
                                &data, &dwSize))
        {
            printf("Connection timeout: %u ms\n\n",data);
        }
        else
        {
            printf( "Error %u in WinHttpQueryOption.\n", 
                    GetLastError());
        }        
        
        // When finished, release the HINTERNET handle.
        WinHttpCloseHandle(hSession);
    }
    else
    {
        printf("Error %u in WinHttpOpen.\n", GetLastError());
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>