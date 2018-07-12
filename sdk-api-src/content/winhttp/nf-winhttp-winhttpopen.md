---
UID: NF:winhttp.WinHttpOpen
title: WinHttpOpen function
author: windows-sdk-content
description: Initializes, for an application, the use of WinHTTP functions and returns a WinHTTP-session handle.
old-location: http\winhttpopen.htm
old-project: winhttp
ms.assetid: 34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33
ms.author: windowssdkdev
ms.date: 03/09/2018
ms.keywords: WINHTTP_ACCESS_TYPE_AUTOMATIC_PROXY, WINHTTP_ACCESS_TYPE_DEFAULT_PROXY, WINHTTP_ACCESS_TYPE_NAMED_PROXY, WINHTTP_ACCESS_TYPE_NO_PROXY, WINHTTP_FLAG_ASYNC, WinHttpOpen, WinHttpOpen function [WinHTTP], http.winhttpopen, winhttp.winhttpopen_function, winhttp/WinHttpOpen
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
 - WinHttpOpen
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpOpen function


## -description


The <b>WinHttpOpen</b> function initializes, for an application, the use of WinHTTP functions and returns a WinHTTP-session handle.


## -parameters




### -param pszAgentW

TBD


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
<li>The <a href="https://msdn.microsoft.com/f96adf59-59be-414e-ad6f-9eac05f4b975">proxycfg.exe</a> utility on Windows XP and Windows Server 2003 or earlier.</li>
<li>The <a href="http://go.microsoft.com/fwlink/p/?linkid=186359">netsh.exe</a> utility  on Windows Vista and Windows Server 2008 or later.</li>
<li>
<a href="https://msdn.microsoft.com/df95703b-8fa0-4ea4-b9e6-7f19aa8c1941">WinHttpSetDefaultProxyConfiguration</a> on all platforms.</li>
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
 


### -param pszProxyW

TBD


### -param pszProxyBypassW

TBD


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
Use the WinHTTP functions asynchronously.  By default, all WinHTTP functions that use the returned 
<a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> handle are performed synchronously.  When this flag is set, the caller needs to specify a callback function through <a href="https://msdn.microsoft.com/b093daf0-7abe-49cb-8c09-9519e3c130b6">WinHttpSetStatusCallback</a>.

</td>
</tr>
</table>
 


#### - pwszProxyBypass [in]

A pointer to a string variable that contains an optional semicolon delimited list of host names or IP addresses, or both, that should not be routed through the proxy when 
<i>dwAccessType</i> is set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>. The list can contain wildcard characters. Do not use an empty string, because the 
<b>WinHttpOpen</b> function  uses it as the proxy bypass list. If this parameter specifies the "&lt;local&gt;" macro in the list as the only entry, this function bypasses any host name that does not contain a period. If 
<i>dwAccessType</i> is not set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>, this parameter must be set to <b>WINHTTP_NO_PROXY_BYPASS</b>.


#### - pwszProxyName [in]

A pointer to a string variable that contains the name of the proxy server to use when proxy access is specified by setting 
<i>dwAccessType</i> to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>.  The WinHTTP functions recognize only CERN type proxies for HTTP. If 
<i>dwAccessType</i> is not set to 
<b>WINHTTP_ACCESS_TYPE_NAMED_PROXY</b>, this parameter must be set to <b>WINHTTP_NO_PROXY_NAME</b>.


#### - pwszUserAgent [in, optional]

A pointer to a string variable that contains the name of the application or entity calling the WinHTTP functions. This name is used as the <a href="glossary.htm">user agent</a> in the HTTP protocol.


## -returns



Returns a valid session handle if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call 
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



Even when  WinHTTP is  used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <b>WinHttpOpen</b>), this function operates synchronously. The return value indicates success or failure.  To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The 
<b>WinHttpOpen</b> function is the first of the WinHTTP functions called by an application. It initializes internal WinHTTP data structures and prepares for future calls from the application. When the application finishes using the WinHTTP functions, it must call 
<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a> to free the session handle and any associated resources.

The application can make any number of calls to 
<b>WinHttpOpen</b>, though a single call is normally sufficient.  Each call to 
<b>WinHttpOpen</b> opens a new session context.  Because user data is not shared between multiple session contexts, an application that makes requests on behalf of multiple users should create a separate session for each user, so as not to share user-specific cookies and authentication state. The application should define separate behaviors for each 
<b>WinHttpOpen</b> instance, such as different proxy servers configured for each.

After the calling application has finished using the 
<a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> handle returned by 
<b>WinHttpOpen</b>, it must be closed using the 
<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a> function.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a>.</div>
<div> </div>

#### Examples

The following example code shows how to retrieve the default connection 
                time-out value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
                                &amp;data, &amp;dwSize))
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>
 

 

