---
UID: NF:wininet.HttpSendRequestA
title: HttpSendRequestA function
author: windows-sdk-content
description: Sends the specified request to the HTTP server, allowing callers to send extra data beyond what is normally passed to HttpSendRequestEx.
old-location: wininet\httpsendrequest.htm
old-project: WinInet
ms.assetid: f53d9ff7-43b1-452f-a6cb-754d0229ab9a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: HttpSendRequest, HttpSendRequest function [WinINet], HttpSendRequestA, HttpSendRequestW, _inet_httpsendrequest_function, wininet.httpsendrequest, wininet/HttpSendRequest, wininet/HttpSendRequestA, wininet/HttpSendRequestW
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
req.unicode-ansi: HttpSendRequestW (Unicode) and HttpSendRequestA (ANSI)
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
 - HttpSendRequest
 - HttpSendRequestA
 - HttpSendRequestW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# HttpSendRequestA function


## -description


Sends the specified request to the HTTP server, allowing callers to send extra data beyond what is normally passed to <a href="https://msdn.microsoft.com/3362fcd2-e8df-4886-9525-bf60589b2c1f">HttpSendRequestEx</a>.


## -parameters




### -param hRequest [in]

A handle returned by 
a call to the <a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> function.


### -param lpszHeaders [in]

A pointer to a <b>null</b>-terminated string  that contains the additional headers to be appended to the request. This parameter can be <b>NULL</b> if there are no additional headers to be appended.


### -param dwHeadersLength [in]

The size of the additional headers, in <b>TCHARs</b>. If this parameter is -1L and 
<i>lpszHeaders</i> is not <b>NULL</b>, the function assumes that 
<i>lpszHeaders</i> is zero-terminated (ASCIIZ), and the length is calculated. See Remarks for specifics.


### -param lpOptional [in]

A pointer to a buffer containing any optional data to be sent immediately after the request headers. This parameter is generally used for POST and PUT operations. The optional data can be the resource or information being posted to the server. This parameter can be <b>NULL</b> if there is no optional data to send.


### -param dwOptionalLength [in]

The size of the optional data, in bytes. This parameter can be zero if there is no optional data to send.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>HttpSendRequest</b> sends the specified request to the HTTP server and allows the client to specify additional headers to send along with the request.

The function also lets the client specify optional data to send to the HTTP server immediately following the request headers. This feature is generally used for "write" operations such as PUT and POST.

After the request is sent, the status code and response headers from the HTTP server are read. These headers are maintained internally and are available to client applications through the 
<a href="https://msdn.microsoft.com/5747ce19-5004-4eea-abe9-dd00abac1b3b">HttpQueryInfo</a> function.

An application can use the same HTTP request handle in multiple calls to 
<b>HttpSendRequest</b>, but the application must read all data returned from the previous call before calling the function again.

In offline mode, 
<b>HttpSendRequest</b> returns <b>ERROR_FILE_NOT_FOUND</b> if the resource is not found in the Internet cache.

There two versions of 
<b>HttpSendRequest</b>—<b>HttpSendRequestA</b> (used with ANSI builds) and <b>HttpSendRequestW</b> (used with Unicode builds).  If 
<b>dwHeadersLength</b> is -1L and 
<i>lpszHeaders</i> is not <b>NULL</b>, the following will happen:  If <b>HttpSendRequestA</b> is called, the function assumes that 
<i>lpszHeaders</i> is zero-terminated (ASCIIZ), and the length is calculated.  If <b>HttpSendRequestW</b> is called, the function fails with <b>ERROR_INVALID_PARAMETER</b>.

<div class="alert"><b>Note</b>  The <b>HttpSendRequestA</b> function  represents headers as ISO-8859-1 characters not ANSI characters. The <b>HttpSendRequestW</b> function represents headers as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpSendRequestW</b> function when the headers to be added can contain non-ASCII characters.
Instead, an application can use the <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> and <a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f307e28-9c38-41e7-9795-7eef08e99a3c">HTTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

