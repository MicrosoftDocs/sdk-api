---
UID: NF:winhttp.WinHttpGetDefaultProxyConfiguration
title: WinHttpGetDefaultProxyConfiguration function
author: windows-sdk-content
description: Retrieves the default WinHTTP proxy configuration from the registry.
old-location: http\winhttpgetdefaultproxyconfiguration.htm
old-project: winhttp
ms.assetid: e8038b4b-b9d0-481a-a49c-26201d72bc7a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WinHttpGetDefaultProxyConfiguration, WinHttpGetDefaultProxyConfiguration function [WinHTTP], http.winhttpgetdefaultproxyconfiguration, winhttp.winhttpgetdefaultproxyconfiguration_function, winhttp/WinHttpGetDefaultProxyConfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WinHttpGetDefaultProxyConfiguration
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpGetDefaultProxyConfiguration function


## -description


The <b>WinHttpGetDefaultProxyConfiguration</b> function retrieves the default WinHTTP proxy configuration from the registry.


## -parameters




### -param pProxyInfo [in, out]

A pointer to a variable of type 
<a href="https://msdn.microsoft.com/acb51bc5-43e2-4657-96eb-8e3d3e82e018">WINHTTP_PROXY_INFO</a> that receives the default proxy configuration.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To retrieve a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Error codes returned include the following.

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
<a href="https://msdn.microsoft.com/df95703b-8fa0-4ea4-b9e6-7f19aa8c1941">WinHttpSetDefaultProxyConfiguration</a> or 
<a href="https://msdn.microsoft.com/f96adf59-59be-414e-ad6f-9eac05f4b975">ProxyCfg.exe</a>.

The default proxy configuration can be overridden for a WinHTTP session by calling 
<a href="https://msdn.microsoft.com/bcf1da09-5787-4d2a-82ae-6965e27fa477">WinHttpSetOption</a> and specifying the 
<a href="https://msdn.microsoft.com/en-us/library/Aa384066(v=VS.85).aspx">WINHTTP_OPTION_PROXY</a> flag.  
<b>WinHttpGetDefaultProxyConfiguration</b> does not retrieve the configuration for the current session.  It retrieves the configuration specified in the registry.

If the registry contains a list of proxy servers, the 
<b>dwAccessType</b> member of 
<i>pProxyInfo</i> is set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>.  Otherwise, it is set to 
<b>WINHTTP_ACCESS_TYPE_NO_PROXY</b>.

<b>WinHttpGetDefaultProxyConfiguration</b> allocates memory for the string members of 
<i>pProxyInfo</i>.  To free this memory, call <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHTTP Start Page.</div>
<div> </div>

#### Examples

The following code example shows how to retrieve the default proxy configuration from the registry.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    WINHTTP_PROXY_INFO proxyInfo;

    // Retrieve the default proxy configuration.
    WinHttpGetDefaultProxyConfiguration( &amp;proxyInfo );

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f96adf59-59be-414e-ad6f-9eac05f4b975">ProxyCfg.exe, a Proxy Configuration Tool</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/df95703b-8fa0-4ea4-b9e6-7f19aa8c1941">WinHttpSetDefaultProxyConfiguration</a>
 

 

