---
UID: NF:wininet.HttpSendRequestExW
title: HttpSendRequestExW function (wininet.h)
description: Sends the specified request to the HTTP server. (HttpSendRequestExW)
helpviewer_keywords: ["HttpSendRequestEx", "HttpSendRequestEx function [WinINet]", "HttpSendRequestExW", "_win32_httpsendrequestex", "wininet.httpsendrequestex", "wininet/HttpSendRequestEx", "wininet/HttpSendRequestExW"]
old-location: wininet\httpsendrequestex.htm
tech.root: wininet
ms.assetid: 3362fcd2-e8df-4886-9525-bf60589b2c1f
ms.date: 12/05/2018
ms.keywords: HttpSendRequestEx, HttpSendRequestEx function [WinINet], HttpSendRequestExA, HttpSendRequestExW, _win32_httpsendrequestex, wininet.httpsendrequestex, wininet/HttpSendRequestEx, wininet/HttpSendRequestExA, wininet/HttpSendRequestExW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpSendRequestExW
 - wininet/HttpSendRequestExW
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
 - HttpSendRequestEx
 - HttpSendRequestExA
 - HttpSendRequestExW
---

# HttpSendRequestExW function


## -description

Sends the specified request to the HTTP server.
<div class="alert"><b>Note</b>  Callers that need to send extra data beyond what is normally passed to <b>HttpSendRequestEx</b> can do so by calling <a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a> instead.</div><div> </div>

## -parameters

### -param hRequest [in]

A 
						handle returned by 
a call to the <a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

### -param lpBuffersIn [in]

Optional. A pointer to an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_buffersa">INTERNET_BUFFERS</a> structure.

### -param lpBuffersOut [out]

Reserved. Must be <b>NULL</b>.

### -param dwFlags [in]

Reserved. Must be zero.

### -param dwContext [in]

Application-defined context value, if a status callback function has been registered.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>HttpSendRequestEx</b> performs  both the send and the receive for the response.  This does not allow the application to send any extra data beyond the single buffer that was passed to <b>HttpSendRequestEx</b>. Callers that need to send extra data beyond what is normally passed to <b>HttpSendRequestEx</b> can do so by calling <a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a> instead.   After the call to <b>HttpSendRequestEx</b>, send the remaining data by calling <a href="/windows/desktop/api/wininet/nf-wininet-internetwritefile">InternetWriteFile</a>.  Finally, follow up with a call to <a href="/windows/desktop/api/wininet/nf-wininet-httpendrequesta">HttpEndRequest</a>.  

<div class="alert"><b>Note</b>  The <b>HttpSendRequestExA</b> function  represents data to send as ISO-8859-1 characters not ANSI characters. The <b>HttpSendRequestExW</b> function represents data to send as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpSendRequestExW</b> function when the headers to be added can contain non-ASCII characters.
Instead, an application can use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines HttpSendRequestEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-sessions">HTTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
