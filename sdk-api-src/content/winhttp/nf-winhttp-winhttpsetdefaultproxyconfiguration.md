---
UID: NF:winhttp.WinHttpSetDefaultProxyConfiguration
title: WinHttpSetDefaultProxyConfiguration function
author: windows-sdk-content
description: Sets the default WinHTTP proxy configuration in the registry.
old-location: http\winhttpsetdefaultproxyconfiguration.htm
old-project: winhttp
ms.assetid: df95703b-8fa0-4ea4-b9e6-7f19aa8c1941
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WinHttpSetDefaultProxyConfiguration, WinHttpSetDefaultProxyConfiguration function [WinHTTP], http.winhttpsetdefaultproxyconfiguration, winhttp.winhttpsetdefaultproxyconfiguration_function, winhttp/WinHttpSetDefaultProxyConfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winhttp.h
req.include-header: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
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
tech.root: 
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpSetDefaultProxyConfiguration function


## -description


The <b>WinHttpSetDefaultProxyConfiguration</b> function sets the default WinHTTP proxy configuration in the registry.


## -parameters




### -param pProxyInfo [in]

A pointer to a variable of type 
<a href="https://msdn.microsoft.com/acb51bc5-43e2-4657-96eb-8e3d3e82e018">WINHTTP_PROXY_INFO</a> that specifies the default proxy configuration.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned are the following.

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
<a href="https://msdn.microsoft.com/f96adf59-59be-414e-ad6f-9eac05f4b975">ProxyCfg.exe</a>.

The default proxy configuration set by this function can be overridden for an existing WinHTTP session by calling 
<a href="https://msdn.microsoft.com/bcf1da09-5787-4d2a-82ae-6965e27fa477">WinHttpSetOption</a> and specifying the 
<a href="https://msdn.microsoft.com/en-us/library/Aa384066(v=VS.85).aspx">WINHTTP_OPTION_PROXY</a> flag.  The default proxy configuration can be overridden for a new session by specifying the configuration with the 
<a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a> function.

The 
<b>dwAccessType</b> member of 
the <a href="https://msdn.microsoft.com/acb51bc5-43e2-4657-96eb-8e3d3e82e018">WINHTTP_PROXY_INFO</a> structure pointed to by <i>pProxyInfo</i> should be set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b> if a proxy is specified.  Otherwise, it should be set to 
<b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b>.

Any new sessions created after calling this function use the new default proxy configuration.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHTTP start page.</div>
<div> </div>

#### Examples

The following code example shows how to set the default proxy configuration in the registry.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    WINHTTP_PROXY_INFO proxyInfo;

    // Allocate memory for string members.
    proxyInfo.lpszProxy = new WCHAR[25];
    proxyInfo.lpszProxyBypass = new WCHAR[25];
    
    // Set the members of the proxy info structure.
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    swprintf_s(proxyInfo.lpszProxy, 25, L"proxy_server");
    swprintf_s(proxyInfo.lpszProxyBypass, 25, L"&lt;local&gt;");

    // Set the default proxy configuration.
    if (WinHttpSetDefaultProxyConfiguration( &amp;proxyInfo ))
        printf("Proxy Configuration Set.\n");

    // Free memory allocated to the strings.
    delete [] proxyInfo.lpszProxy;
    delete [] proxyInfo.lpszProxyBypass;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f96adf59-59be-414e-ad6f-9eac05f4b975">ProxyCfg.exe, a Proxy Configuration Tool</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/e8038b4b-b9d0-481a-a49c-26201d72bc7a">WinHttpGetDefaultProxyConfiguration</a>
 

 

