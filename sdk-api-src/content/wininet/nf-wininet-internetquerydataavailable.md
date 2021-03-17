---
UID: NF:wininet.InternetQueryDataAvailable
title: InternetQueryDataAvailable function (wininet.h)
description: Queries the server to determine the amount of data available.
helpviewer_keywords: ["InternetQueryDataAvailable","InternetQueryDataAvailable function [WinINet]","_inet_internetquerydataavailable_function","wininet.internetquerydataavailable","wininet/InternetQueryDataAvailable"]
old-location: wininet\internetquerydataavailable.htm
tech.root: wininet
ms.assetid: fea8250d-f260-421f-b4dd-14b8685e8dac
ms.date: 12/05/2018
ms.keywords: InternetQueryDataAvailable, InternetQueryDataAvailable function [WinINet], _inet_internetquerydataavailable_function, wininet.internetquerydataavailable, wininet/InternetQueryDataAvailable
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - InternetQueryDataAvailable
 - wininet/InternetQueryDataAvailable
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
 - InternetQueryDataAvailable
---

# InternetQueryDataAvailable function


## -description

Queries the server to determine the amount of data available.

## -parameters

### -param hFile [in]

Handle returned by 
the <a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a>, 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>, 
<a href="/windows/desktop/api/wininet/nf-wininet-gopheropenfilea">GopherOpenFile</a>, or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

### -param lpdwNumberOfBytesAvailable [out]

Pointer to a variable that receives the number of available bytes. May be <b>NULL</b>.

### -param dwFlags [in]

This parameter is reserved and must be 0.

### -param dwContext [in]

This parameter is reserved and must be 0.

## -returns

Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns ERROR_NO_MORE_FILES.

## -remarks

This function returns the number of bytes of data that are available to be read immediately by a subsequent call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfile">InternetReadFile</a>. If there is currently no data available and the end of the file has not been reached, the request waits until data becomes available. The amount of data remaining will not be recalculated until all available data indicated by the call to 
<b>InternetQueryDataAvailable</b> is read.

For 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handles created by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> and sent by 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>, a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-httpendrequesta">HttpEndRequest</a> must be made on the handle before 
<b>InternetQueryDataAvailable</b> can be used.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>