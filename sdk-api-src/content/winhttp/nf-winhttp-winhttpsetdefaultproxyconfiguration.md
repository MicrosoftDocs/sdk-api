---
UID: NF:winhttp.WinHttpSetDefaultProxyConfiguration
title: WinHttpSetDefaultProxyConfiguration function (winhttp.h)
author: windows-sdk-content
description: Sets the default WinHTTP proxy configuration in the registry.
old-location: http\winhttpsetdefaultproxyconfiguration.htm
tech.root: WinHttp
ms.assetid: df95703b-8fa0-4ea4-b9e6-7f19aa8c1941
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WinHttpSetDefaultProxyConfiguration, WinHttpSetDefaultProxyConfiguration function [WinHTTP], http.winhttpsetdefaultproxyconfiguration, winhttp.winhttpsetdefaultproxyconfiguration_function, winhttp/WinHttpSetDefaultProxyConfiguration
ms.topic: function
f1_keywords: 
 - "winhttp/WinHttpSetDefaultProxyConfiguration"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpSetDefaultProxyConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
---

# WinHttpSetDefaultProxyConfiguration function


## -description


The <b>WinHttpSetDefaultProxyConfiguration</b> function sets the default WinHTTP proxy configuration in the registry.


## -parameters




### -param pProxyInfo [in]

A pointer to a variable of type 
<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/ns-winhttp-__unnamed_struct_3">WINHTTP_PROXY_INFO</a> that specifies the default proxy configuration.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

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



<b>WinHttpSetDefaultProxyConfiguration</b> changes the proxy configuration set by 
<a href="https://docs.microsoft.com/windows/desktop/WinHttp/proxycfg-exe--a-proxy-configuration-tool">ProxyCfg.exe</a>.

The default proxy configuration set by this function can be overridden for an existing WinHTTP session by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> and specifying the 
<a href="https://docs.microsoft.com/windows/desktop/WinHttp/option-flags">WINHTTP_OPTION_PROXY</a> flag.  The default proxy configuration can be overridden for a new session by specifying the configuration with the 
<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a> function.

The 
<b>dwAccessType</b> member of 
the <a href="https://docs.microsoft.com/windows/desktop/api/winhttp/ns-winhttp-__unnamed_struct_3">WINHTTP_PROXY_INFO</a> structure pointed to by <i>pProxyInfo</i> should be set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b> if a proxy is specified.  Otherwise, it should be set to 
<b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b>.

Any new sessions created after calling this function use the new default proxy configuration.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHTTP start page.</div>
<div> </div>

#### Examples

The following code example shows how to set the default proxy configuration in the registry.


```cpp
    WINHTTP_PROXY_INFO proxyInfo;

    // Allocate memory for string members.
    proxyInfo.lpszProxy = new WCHAR[25];
    proxyInfo.lpszProxyBypass = new WCHAR[25];
    
    // Set the members of the proxy info structure.
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    swprintf_s(proxyInfo.lpszProxy, 25, L"proxy_server");
    swprintf_s(proxyInfo.lpszProxyBypass, 25, L"<local>");

    // Set the default proxy configuration.
    if (WinHttpSetDefaultProxyConfiguration( &proxyInfo ))
        printf("Proxy Configuration Set.\n");

    // Free memory allocated to the strings.
    delete [] proxyInfo.lpszProxy;
    delete [] proxyInfo.lpszProxyBypass;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinHttp/proxycfg-exe--a-proxy-configuration-tool">ProxyCfg.exe, a Proxy Configuration Tool</a>



<a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration">WinHttpGetDefaultProxyConfiguration</a>
 

 

