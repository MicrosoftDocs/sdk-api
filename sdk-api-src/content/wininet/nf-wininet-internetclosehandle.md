---
UID: NF:wininet.InternetCloseHandle
title: InternetCloseHandle function (wininet.h)
author: windows-sdk-content
description: Closes a single Internet handle.
old-location: wininet\internetclosehandle.htm
tech.root: wininet
ms.assetid: 52b57e3c-3cfe-40bc-b87b-90cf39c5c38d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InternetCloseHandle, InternetCloseHandle function [WinINet], _win32_internetclosehandle, wininet.internetclosehandle, wininet/InternetCloseHandle
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetCloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetCloseHandle function


## -description


Closes a single Internet handle.


## -parameters




### -param hInternet [in]

Handle to be closed.


## -returns



Returns <b>TRUE</b> if the handle is successfully closed, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function terminates any pending operations on the handle and discards any outstanding data. 


It is safe to call <b>InternetCloseHandle</b> as long as no API calls are being made or will be made using the handle.  Once an API has returned <b>ERROR_IO_PENDING</b>, it is safe to call <b>InternetCloseHandle</b> to cancel that I/O, as long as no subsequent API calls will be issued with the handle. 

It is safe to call <b>InternetCloseHandle</b> in a callback for the handle being closed. If there is a status callback registered for the handle being closed, and the handle was created with a non-NULL context value, an <b>INTERNET_STATUS_HANDLE_CLOSING</b> callback will be made. This indication will be the last callback made from a handle and indicates that the handle is being destroyed.

If asynchronous requests are pending for the handle or any of its child handles, the handle cannot be closed immediately, but it will be invalidated. Any new requests attempted using the handle will return with an 
<a href="https://msdn.microsoft.com/338bf65f-ebe5-4434-8407-9ab2a4c8d381">ERROR_INVALID_HANDLE</a> notification. The asynchronous requests will complete with <b>INTERNET_STATUS_REQUEST_COMPLETE</b>. Applications must be prepared to receive any <b>INTERNET_STATUS_REQUEST_COMPLETE</b> indications on the handle before the final <b>INTERNET_STATUS_HANDLE_CLOSING</b> indication is made, which indicates that the handle is completely closed.

An application can call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to determine if requests are pending. If 
<b>GetLastError</b> returns <b>ERROR_IO_PENDING</b>, there were outstanding requests when the handle was closed.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/80747c0d-5a09-4ffa-a0ca-b051b82acbf8">Enabling Internet Functionality</a>



<a href="https://msdn.microsoft.com/4f331f99-c52c-4744-a9a7-eeb09803862d">FtpFindFirstFile</a>



<a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a>



<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a>



<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a>



<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

