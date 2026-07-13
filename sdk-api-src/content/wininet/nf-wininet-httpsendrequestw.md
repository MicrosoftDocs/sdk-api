---
UID: NF:wininet.HttpSendRequestW
title: HttpSendRequestW function (wininet.h)
description: Sends the specified request to the HTTP server, allowing callers to send extra data beyond what is normally passed to HttpSendRequestEx. (Unicode)
helpviewer_keywords: ["HttpSendRequest", "HttpSendRequest function [WinINet]", "HttpSendRequestW", "_inet_httpsendrequest_function", "wininet.httpsendrequest", "wininet/HttpSendRequest", "wininet/HttpSendRequestW"]
old-location: wininet\httpsendrequest.htm
tech.root: wininet
ms.assetid: f53d9ff7-43b1-452f-a6cb-754d0229ab9a
ms.date: 12/05/2018
ms.keywords: HttpSendRequest, HttpSendRequest function [WinINet], HttpSendRequestA, HttpSendRequestW, _inet_httpsendrequest_function, wininet.httpsendrequest, wininet/HttpSendRequest, wininet/HttpSendRequestA, wininet/HttpSendRequestW
req.header: wininet.h
req.include-header: 
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpSendRequestW
 - wininet/HttpSendRequestW
dev_langs:
 - c++
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
---

# HttpSendRequestW function


## -description

Sends the specified request to the HTTP server, allowing callers to send extra data beyond what is normally passed to <a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>.

## -parameters

### -param hRequest [in]

A handle returned by 
a call to the <a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>HttpSendRequest</b> sends the specified request to the HTTP server and allows the client to specify additional headers to send along with the request.

The function also lets the client specify optional data to send to the HTTP server immediately following the request headers. This feature is generally used for "write" operations such as PUT and POST.

After the request is sent, the status code and response headers from the HTTP server are read. These headers are maintained internally and are available to client applications through the 
<a href="/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa">HttpQueryInfo</a> function.

An application can use the same HTTP request handle in multiple calls to 
<b>HttpSendRequest</b>, but the application must read all data returned from the previous call before calling the function again.

In offline mode, 
<b>HttpSendRequest</b> returns <b>ERROR_FILE_NOT_FOUND</b> if the resource is not found in the Internet cache.

There are two versions of 
<b>HttpSendRequest</b>—<b>HttpSendRequestA</b> (used with ANSI builds) and <b>HttpSendRequestW</b> (used with Unicode builds).  If 
<b>dwHeadersLength</b> is -1L and 
<i>lpszHeaders</i> is not <b>NULL</b>, the following will happen:  If <b>HttpSendRequestA</b> is called, the function assumes that 
<i>lpszHeaders</i> is zero-terminated (ASCIIZ), and the length is calculated.  If <b>HttpSendRequestW</b> is called, the function fails with <b>ERROR_INVALID_PARAMETER</b>.

<div class="alert"><b>Note</b>  The <b>HttpSendRequestA</b> function  represents headers as ISO-8859-1 characters not ANSI characters. The <b>HttpSendRequestW</b> function represents headers as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpSendRequestW</b> function when the headers to be added can contain non-ASCII characters.
Instead, an application can use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines HttpSendRequest as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-sessions">HTTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
