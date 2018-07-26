---
UID: NF:wininet.HttpQueryInfoW
title: HttpQueryInfoW function
author: windows-sdk-content
description: Retrieves header information associated with an HTTP request.
old-location: wininet\httpqueryinfo.htm
old-project: wininet
ms.assetid: 5747ce19-5004-4eea-abe9-dd00abac1b3b
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: HttpQueryInfo, HttpQueryInfo function [WinINet], HttpQueryInfoA, HttpQueryInfoW, _inet_httpqueryinfo_function, wininet.httpqueryinfo, wininet/HttpQueryInfo, wininet/HttpQueryInfoA, wininet/HttpQueryInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpQueryInfoW (Unicode) and HttpQueryInfoA (ANSI)
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
 - HttpQueryInfo
 - HttpQueryInfoA
 - HttpQueryInfoW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# HttpQueryInfoW function


## -description


Retrieves header information associated with an HTTP request.


## -parameters




### -param hRequest [in]


						A handle returned by 
a call to the <a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> or 
<a href="https://msdn.microsoft.com/73f969c3-3fa7-43f5-88c5-ba78e59a8d1c">InternetOpenUrl</a> function.


### -param dwInfoLevel [in]

A combination of an attribute to be retrieved and flags that modify the request. For a list of possible attribute and modifier values, see 
<a href="https://msdn.microsoft.com/b1613193-ae03-411e-bf05-de42f471cd8c">Query Info Flags</a>.


### -param lpBuffer

TBD


### -param lpdwBufferLength [in, out]

A pointer to a variable that contains, on entry, the size in bytes of the buffer pointed to by <i>lpvBuffer</i>. 

When the function returns successfully, this variable contains the number of bytes of information written to the buffer. In the case of a string, the byte count does not include the string's terminating <b>null</b> character.

When the function  
					fails with an extended error code of <b>ERROR_INSUFFICIENT_BUFFER</b>, the variable pointed to by <i>lpdwBufferLength</i> contains on exit the size, in bytes, of a buffer large enough to receive the requested information. The calling application can then allocate a buffer of this size or larger, and call the function again.


### -param lpdwIndex [in, out]

A pointer to a zero-based header index used to enumerate multiple headers with the same name. When calling the function, this parameter is the index of the specified header to return. When the function returns, this parameter is the index of the next header. If the next index cannot be found, <b>ERROR_HTTP_HEADER_NOT_FOUND</b> is returned.


#### - lpvBuffer [in, out]

A pointer to a buffer to receive the requested information. This parameter must not be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can retrieve the following types of data from 
<b>HttpQueryInfo</b>:<ul>
<li>Strings (default)</li>
<li>
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> (for dates)</li>
<li><b>DWORD</b> (for <b>STATUS_CODE</b>, <b>CONTENT_LENGTH</b>, and so on, if <b>HTTP_QUERY_FLAG_NUMBER</b> has been used)</li>
</ul>


If your application requires that the data be returned as a data type other than a string, you must include the appropriate modifier with the attribute passed to 
<i>dwInfoLevel</i>.


				The <b>HttpQueryInfo</b> function is available in Microsoft Internet Explorer 3.0 for ISO-8859-1 characters (<b>HttpQueryInfoA</b> function) and in Internet Explorer 4.0 or later for ISO-8859-1 characters (<b>HttpQueryInfoA</b> function)  and for ISO-8859-1  characters converted to UTF-16LE  characters.(the <b>HttpQueryInfoW</b> function). 

<div class="alert"><b>Note</b>  The <b>HttpQueryInfoA</b> function represents headers as ISO-8859-1 characters not ANSI characters. The <b>HttpQueryInfoW</b> function represents headers as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpQueryInfoW</b> function when the headers can contain non-ASCII characters.
Instead, an application can use the <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> and <a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
See <a href="https://msdn.microsoft.com/347e4fb3-5f96-488a-bef8-4df0b8d1ade1">Retrieving HTTP Headers</a> for an example code calling the <b>HttpQueryInfo</b> function.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f307e28-9c38-41e7-9795-7eef08e99a3c">HTTP Sessions</a>



<a href="https://msdn.microsoft.com/347e4fb3-5f96-488a-bef8-4df0b8d1ade1">Retrieving HTTP Headers</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

