---
UID: NF:winhttp.WinHttpGetDefaultProxyConfiguration
title: WinHttpGetDefaultProxyConfiguration function (winhttp.h)
description: Retrieves the default WinHTTP proxy configuration from the registry.
helpviewer_keywords: ["WinHttpGetDefaultProxyConfiguration","WinHttpGetDefaultProxyConfiguration function [WinHTTP]","http.winhttpgetdefaultproxyconfiguration","winhttp.winhttpgetdefaultproxyconfiguration_function","winhttp/WinHttpGetDefaultProxyConfiguration"]
old-location: http\winhttpgetdefaultproxyconfiguration.htm
tech.root: http
ms.assetid: e8038b4b-b9d0-481a-a49c-26201d72bc7a
ms.date: 12/05/2018
ms.keywords: WinHttpGetDefaultProxyConfiguration, WinHttpGetDefaultProxyConfiguration function [WinHTTP], http.winhttpgetdefaultproxyconfiguration, winhttp.winhttpgetdefaultproxyconfiguration_function, winhttp/WinHttpGetDefaultProxyConfiguration
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
 - WinHttpGetDefaultProxyConfiguration
 - winhttp/WinHttpGetDefaultProxyConfiguration
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
 - WinHttpGetDefaultProxyConfiguration
---

# WinHttpGetDefaultProxyConfiguration function


## -description

The <b>WinHttpGetDefaultProxyConfiguration</b> function retrieves the default WinHTTP proxy configuration from the registry.

## -parameters

### -param pProxyInfo [in, out]

A pointer to a variable of type 
<a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info">WINHTTP_PROXY_INFO</a> that receives the default proxy configuration.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To retrieve a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Error codes returned include the following.

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

<b>WinHttpGetDefaultProxyConfiguration</b> retrieves the proxy configuration set by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration">WinHttpSetDefaultProxyConfiguration</a> or 
<a href="/windows/desktop/WinHttp/proxycfg-exe--a-proxy-configuration-tool">ProxyCfg.exe</a>.

The default proxy configuration can be overridden for a WinHTTP session by calling 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> and specifying the 
<a href="/windows/desktop/WinHttp/option-flags">WINHTTP_OPTION_PROXY</a> flag.  
<b>WinHttpGetDefaultProxyConfiguration</b> does not retrieve the configuration for the current session.  It retrieves the configuration specified in the registry.

If the registry contains a list of proxy servers, the 
<b>dwAccessType</b> member of 
<i>pProxyInfo</i> is set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>.  Otherwise, it is set to 
<b>WINHTTP_ACCESS_TYPE_NO_PROXY</b>.

<b>WinHttpGetDefaultProxyConfiguration</b> allocates memory for the string members of 
<i>pProxyInfo</i>.  To free this memory, call <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a>.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHTTP Start Page.</div>
<div> </div>

#### Examples

The following code example shows how to retrieve the default proxy configuration from the registry.


```cpp
    WINHTTP_PROXY_INFO proxyInfo;

    // Retrieve the default proxy configuration.
    WinHttpGetDefaultProxyConfiguration( &proxyInfo );

    // Display the proxy servers and free memory 
    // allocated to this string.
    if (proxyInfo.lpszProxy != NULL)
    {
        printf("Proxy server list: %S\n", proxyInfo.lpszProxy);
        GlobalFree( proxyInfo.lpszProxy );
    }

    // Display the bypass list and free memory 
    // allocated to this string.
    if (proxyInfo.lpszProxyBypass != NULL)
    {
        printf("Proxy bypass list: %S\n", proxyInfo.lpszProxyBypass);
        GlobalFree( proxyInfo.lpszProxyBypass );
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/proxycfg-exe--a-proxy-configuration-tool">ProxyCfg.exe, a Proxy Configuration Tool</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration">WinHttpSetDefaultProxyConfiguration</a>