---
UID: NF:wininet.HttpOpenRequestW
title: HttpOpenRequestW function
author: windows-sdk-content
description: Creates an HTTP request handle.
old-location: wininet\httpopenrequest.htm
old-project: WinInet
ms.assetid: caaff8e8-7db9-4d6d-8ba2-d8d19475173a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: HTTP/1.0, HTTP/1.1, HttpOpenRequest, HttpOpenRequest function [WinINet], HttpOpenRequestA, HttpOpenRequestW, _inet_httpopenrequest_function, wininet.httpopenrequest, wininet/HttpOpenRequest, wininet/HttpOpenRequestA, wininet/HttpOpenRequestW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpOpenRequestW (Unicode) and HttpOpenRequestA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - HttpOpenRequest
 - HttpOpenRequestA
 - HttpOpenRequestW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# HttpOpenRequestW function


## -description


Creates an HTTP request handle.


## -parameters




### -param hConnect [in]

A 
						handle to an HTTP session returned by 
<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a>.


### -param lpszVerb [in]

A pointer to a <b>null</b>-terminated string that contains the HTTP verb to use in the request. If this parameter is <b>NULL</b>, the function uses GET as the HTTP verb.


### -param lpszObjectName [in]

A pointer to a <b>null</b>-terminated string that contains the name of the target object of the specified HTTP verb. This is generally a file name, an executable module, or a search specifier.


### -param lpszVersion [in]

A pointer to a <b>null</b>-terminated string that contains the HTTP version to use in the request. Settings in Internet Explorer will override the value specified in this parameter. 

If this parameter is <b>NULL</b>, the function uses an HTTP version of 1.1 or 1.0, depending on the value of the Internet Explorer settings. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_1.0"></a><a id="http_1.0"></a><dl>
<dt><b>HTTP/1.0</b></dt>
</dl>
</td>
<td width="60%">
HTTP version 1.0

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_1.1"></a><a id="http_1.1"></a><dl>
<dt><b>HTTP/1.1</b></dt>
</dl>
</td>
<td width="60%">
HTTP version 1.1

</td>
</tr>
</table>
 


### -param lpszReferrer [in]

A pointer to a <b>null</b>-terminated string that specifies the URL of the document from which the URL in the request (<i>lpszObjectName</i>) was obtained. If this parameter is <b>NULL</b>, no referrer is specified.


### -param lplpszAcceptTypes [in]

A pointer to a <b>null</b>-terminated array of strings that indicates media types accepted by the client. Here is an example.

<code>PCTSTR rgpszAcceptTypes[] = {_T(“text/*”), NULL};</code>

 Failing to properly terminate the array with a NULL pointer will cause a crash.

If this parameter is <b>NULL</b>, no types are accepted by the client. Servers generally interpret a lack of accept types to indicate that the client accepts only documents of type "text/*" (that is, only text documents—no pictures or other binary files). For more information and  a list of valid media types, see  
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84521">ftp://ftp.isi.edu/in-notes/iana/assignments/media-types/media-types</a>.


### -param dwFlags [in]

Internet options. This parameter can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_CACHE_IF_NET_FAIL</dt>
</dl>
</td>
<td width="60%">
Returns the resource from the cache if the network request for the resource fails due to an ERROR_INTERNET_CONNECTION_RESET (the connection with the server has been reset) or ERROR_INTERNET_CANNOT_CONNECT (the attempt to connect to the server failed).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_HYPERLINK</dt>
</dl>
</td>
<td width="60%">
Forces a reload if there was no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_IGNORE_CERT_CN_INVALID</dt>
</dl>
</td>
<td width="60%">
Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request. WinINet functions use a simple check against certificates by comparing for matching host names and simple wildcarding rules.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_IGNORE_CERT_DATE_INVALID</dt>
</dl>
</td>
<td width="60%">
Disables checking of SSL/PCT-based certificates for proper validity dates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP</dt>
</dl>
</td>
<td width="60%">
Disables detection of this special type of redirect. When this flag is used, WinINet functions transparently allow redirects from HTTPS to HTTP URLs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS</dt>
</dl>
</td>
<td width="60%">
Disables detection of this special type of redirect. When this flag is used, WinINet functions transparently allow redirects from HTTP to HTTPS URLs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_KEEP_CONNECTION</dt>
</dl>
</td>
<td width="60%">
Uses keep-alive semantics, if available, for the connection. This flag is required for Microsoft Network (MSN), NT LAN Manager (NTLM), and other types of authentication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NEED_FILE</dt>
</dl>
</td>
<td width="60%">
Causes a temporary file to be created if the file cannot be cached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_AUTH</dt>
</dl>
</td>
<td width="60%">
Does not attempt authentication automatically.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_AUTO_REDIRECT</dt>
</dl>
</td>
<td width="60%">
Does not automatically handle redirection in 
<a href="https://msdn.microsoft.com/f53d9ff7-43b1-452f-a6cb-754d0229ab9a">HttpSendRequest</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_CACHE_WRITE</dt>
</dl>
</td>
<td width="60%">
Does not add the returned entity to the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_COOKIES</dt>
</dl>
</td>
<td width="60%">
Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_NO_UI</dt>
</dl>
</td>
<td width="60%">
Disables the cookie dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_PRAGMA_NOCACHE</dt>
</dl>
</td>
<td width="60%">
Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_RELOAD</dt>
</dl>
</td>
<td width="60%">
Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_RESYNCHRONIZE</dt>
</dl>
</td>
<td width="60%">
Reloads HTTP resources if the resource has been modified since the last time it was downloaded. All FTP resources are reloaded.

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>Gopher resources are also reloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_FLAG_SECURE</dt>
</dl>
</td>
<td width="60%">
Uses secure transaction semantics. This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.

</td>
</tr>
</table>
 


### -param dwContext [in]

  A pointer to a variable that contains the application-defined value that associates this operation with any application data.


## -returns



Returns an HTTP request handle if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>HttpOpenRequest</b> function creates a new HTTP request handle and stores the specified parameters in that handle. An HTTP request handle holds a request to be sent to an HTTP server and contains all RFC822/MIME/HTTP headers to be sent as part of the request.

If a verb other than "GET" or "POST" is specified, <b>HttpOpenRequest</b> automatically sets INTERNET_FLAG_NO_CACHE_WRITE and INTERNET_FLAG_RELOAD for the request.

With Microsoft Internet Explorer 5 and later, if 
<i>lpszVerb</i> is set to "HEAD", the Content-Length header is ignored on responses from HTTP/1.1 servers.

On Windows 7, Windows Server 2008 R2, and later, the <i>lpszVersion</i> parameter is overridden by Internet Explorer settings.  The <b>EnableHttp1_1</b> is a registry value under <b>HKLM\Software\Microsoft\InternetExplorer\AdvacnedOptions\HTTP\GENABLE</b> controlled by Internet Options set in Internet Explorer for the system.  The <b>EnableHttp1_1</b> value defaults to 1. The <b>HttpOpenRequest</b> function upgrades any HTTP version less than 1.1 to HTTP version 1.1 if <b>EnableHttp1_1</b> is set to 1.


After the calling application has finished using the 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handle returned by 
<b>HttpOpenRequest</b>, it must be closed using the 
<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a> function.

<b>Note</b>   When a request is sent in asynchronous mode (the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/9ec087c9-d484-4763-a527-2ea5c1a0cf28">InternetOpen</a> specifies <b>INTERNET_FLAG_ASYNC</b>), and the <i>dwContext</i> parameter is zero (<b>INTERNET_NO_CALLBACK</b>), the callback function set with <a href="https://msdn.microsoft.com/fe15627b-c77b-45c0-8ff6-02faa8512b57">InternetSetStatusCallback</a> on the request handle will not be invoked, however, the call will still be performed in asynchronous mode. 

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f307e28-9c38-41e7-9795-7eef08e99a3c">HTTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

