---
UID: NF:wininet.HttpEndRequestW
title: HttpEndRequestW function (wininet.h)
description: Ends an HTTP request that was initiated by HttpSendRequestEx. (Unicode)
helpviewer_keywords: ["HttpEndRequest", "HttpEndRequest function [WinINet]", "HttpEndRequestW", "_win32_httpendrequest", "wininet.httpendrequest", "wininet/HttpEndRequest", "wininet/HttpEndRequestW"]
old-location: wininet\httpendrequest.htm
tech.root: wininet
ms.assetid: 6ea91da6-0bc2-49b6-a56b-c4224ad73b81
ms.date: 12/05/2018
ms.keywords: HttpEndRequest, HttpEndRequest function [WinINet], HttpEndRequestA, HttpEndRequestW, _win32_httpendrequest, wininet.httpendrequest, wininet/HttpEndRequest, wininet/HttpEndRequestA, wininet/HttpEndRequestW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpEndRequestW (Unicode) and HttpEndRequestA (ANSI)
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
 - HttpEndRequestW
 - wininet/HttpEndRequestW
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
 - HttpEndRequest
 - HttpEndRequestA
 - HttpEndRequestW
---

# HttpEndRequestW function


## -description

Ends an HTTP request that was initiated by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>.

## -parameters

### -param hRequest [in]

Handle returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> and sent by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>.

### -param lpBuffersOut [out, optional]

This parameter is reserved and must be <b>NULL</b>.

### -param dwFlags [in]

This parameter is reserved and must be set to 0.

### -param dwContext [in, optional]

This parameter is reserved and must be set to 0.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If 
<i>lpBuffersOut</i> is not set to <b>NULL</b>, 
<b>HttpEndRequest</b> will return ERROR_INVALID_PARAMETER.
			

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines HttpEndRequest as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-sessions">HTTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
