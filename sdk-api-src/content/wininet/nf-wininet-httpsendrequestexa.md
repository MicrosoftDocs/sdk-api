---
UID: NF:wininet.HttpSendRequestExA
title: HttpSendRequestExA function (wininet.h)
author: windows-sdk-content
description: Sends the specified request to the HTTP server.
old-location: wininet\httpsendrequestex.htm
tech.root: wininet
ms.assetid: 3362fcd2-e8df-4886-9525-bf60589b2c1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HttpSendRequestEx, HttpSendRequestEx function [WinINet], HttpSendRequestExA, HttpSendRequestExW, _win32_httpsendrequestex, wininet.httpsendrequestex, wininet/HttpSendRequestEx, wininet/HttpSendRequestExA, wininet/HttpSendRequestExW
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpSendRequestExW (Unicode) and HttpSendRequestExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - HttpSendRequestEx
 - HttpSendRequestExA
 - HttpSendRequestExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HttpSendRequestExA function


## -description


Sends the specified request to the HTTP server.
<div class="alert"><b>Note</b>  Callers that need to send extra data beyond what is normally passed to <b>HttpSendRequestEx</b> can do so by calling <a href="https://msdn.microsoft.com/f53d9ff7-43b1-452f-a6cb-754d0229ab9a">HttpSendRequest</a> instead.</div><div> </div>

## -parameters




### -param hRequest [in]

A 
						handle returned by 
a call to the <a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> function.


### -param lpBuffersIn [in]

Optional. A pointer to an 
<a href="https://msdn.microsoft.com/9381184d-17f4-46ad-bd09-15c7e653d1b9">INTERNET_BUFFERS</a> structure.


### -param lpBuffersOut [out]

Reserved. Must be <b>NULL</b>.


### -param dwFlags [in]

Reserved. Must be zero.


### -param dwContext [in]

Application-defined context value, if a status callback function has been registered.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>HttpSendRequestEx</b> performs  both the send and the receive for the response.  This does not allow the application to send any extra data beyond the single buffer that was passed to <b>HttpSendRequestEx</b>. Callers that need to send extra data beyond what is normally passed to <b>HttpSendRequestEx</b> can do so by calling <a href="https://msdn.microsoft.com/f53d9ff7-43b1-452f-a6cb-754d0229ab9a">HttpSendRequest</a> instead.   After the call to <b>HttpSendRequestEx</b>, send the remaining data by calling <a href="https://msdn.microsoft.com/3bf8d4d8-9193-4aed-acf9-8d7207b332a5">InternetWriteFile</a>.  Finally, follow up with a call to <a href="https://msdn.microsoft.com/6ea91da6-0bc2-49b6-a56b-c4224ad73b81">HttpEndRequest</a>.  

<div class="alert"><b>Note</b>  The <b>HttpSendRequestExA</b> function  represents data to send as ISO-8859-1 characters not ANSI characters. The <b>HttpSendRequestExW</b> function represents data to send as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpSendRequestExW</b> function when the headers to be added can contain non-ASCII characters.
Instead, an application can use the <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> and <a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f307e28-9c38-41e7-9795-7eef08e99a3c">HTTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

