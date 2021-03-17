---
UID: NF:wininet.InternetCloseHandle
title: InternetCloseHandle function (wininet.h)
description: Closes a single Internet handle.
helpviewer_keywords: ["InternetCloseHandle","InternetCloseHandle function [WinINet]","_win32_internetclosehandle","wininet.internetclosehandle","wininet/InternetCloseHandle"]
old-location: wininet\internetclosehandle.htm
tech.root: wininet
ms.assetid: 52b57e3c-3cfe-40bc-b87b-90cf39c5c38d
ms.date: 12/05/2018
ms.keywords: InternetCloseHandle, InternetCloseHandle function [WinINet], _win32_internetclosehandle, wininet.internetclosehandle, wininet/InternetCloseHandle
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
 - InternetCloseHandle
 - wininet/InternetCloseHandle
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
 - InternetCloseHandle
---

# InternetCloseHandle function


## -description

Closes a single Internet handle.

## -parameters

### -param hInternet [in]

Handle to be closed.

## -returns

Returns <b>TRUE</b> if the handle is successfully closed, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function terminates any pending operations on the handle and discards any outstanding data. 


It is safe to call <b>InternetCloseHandle</b> as long as no API calls are being made or will be made using the handle.  Once an API has returned <b>ERROR_IO_PENDING</b>, it is safe to call <b>InternetCloseHandle</b> to cancel that I/O, as long as no subsequent API calls will be issued with the handle. 

It is safe to call <b>InternetCloseHandle</b> in a callback for the handle being closed. If there is a status callback registered for the handle being closed, and the handle was created with a non-NULL context value, an <b>INTERNET_STATUS_HANDLE_CLOSING</b> callback will be made. This indication will be the last callback made from a handle and indicates that the handle is being destroyed.

If asynchronous requests are pending for the handle or any of its child handles, the handle cannot be closed immediately, but it will be invalidated. Any new requests attempted using the handle will return with an 
<a href="/windows/desktop/WinInet/wininet-errors">ERROR_INVALID_HANDLE</a> notification. The asynchronous requests will complete with <b>INTERNET_STATUS_REQUEST_COMPLETE</b>. Applications must be prepared to receive any <b>INTERNET_STATUS_REQUEST_COMPLETE</b> indications on the handle before the final <b>INTERNET_STATUS_HANDLE_CLOSING</b> indication is made, which indicates that the handle is completely closed.

An application can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to determine if requests are pending. If 
<b>GetLastError</b> returns <b>ERROR_IO_PENDING</b>, there were outstanding requests when the handle was closed.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpfindfirstfilea">FtpFindFirstFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-gopherfindfirstfilea">GopherFindFirstFile</a>



<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>