---
UID: NF:winsock2.WSAGetLastError
title: WSAGetLastError function (winsock2.h)
description: The WSAGetLastError function (winsock2.h) returns the error status for the last Windows Sockets operation that failed. 
helpviewer_keywords: ["WSAGetLastError","WSAGetLastError function [Winsock]","_win32_wsagetlasterror_2","winsock.wsagetlasterror_2","winsock/WSAGetLastError"]
old-location: winsock\wsagetlasterror_2.htm
tech.root: WinSock
ms.assetid: 39e41b66-44ed-46dc-bfc2-65228b669992
ms.date: 08/03/2022
ms.keywords: WSAGetLastError, WSAGetLastError function [Winsock], _win32_wsagetlasterror_2, winsock.wsagetlasterror_2, winsock/WSAGetLastError
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAGetLastError
 - winsock2/WSAGetLastError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAGetLastError
---

# WSAGetLastError function


## -description

The 
<b>WSAGetLastError</b> function returns the error status for the last Windows Sockets operation that failed.



## -returns

The return value indicates the error code for this thread's last Windows Sockets operation that failed.

## -remarks

The 
<b>WSAGetLastError</b> function returns the last error that occurred for the calling thread. When a particular Windows Sockets function indicates an error has occurred, this function should be called immediately to retrieve the extended error code for the failing function call. This extended error code can be different from the error code obtained from 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> when called with an <i>optname</i> parameter of <b>SO_ERROR</b>, which is socket-specific since 
<b>WSAGetLastError</b> is for all thread-specific sockets.

If a function call's return value indicates that error or other relevant data was returned in the error code, <b>WSAGetLastError</b> should be called immediately. This is necessary because some functions may  reset the last extended error code to 0 if they succeed, overwriting the extended error code returned by a previously failed function. To specifically reset the extended error code, use the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a> function call with the <i>iError</i> parameter set to zero. A 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function when called with an <i>optname</i> parameter of <b>SO_ERROR</b> also resets the extended error code to zero.

The 
<b>WSAGetLastError</b> function should not be used to check for an extended error value on receipt of an asynchronous message. In this case, the extended error value is passed in the <i>lParam</i> parameter of the message, and this can differ from the value returned by 
<b>WSAGetLastError</b>.


<div class="alert"><b>Note</b>  An application can call the <b>WSAGetLastError</b> function to determine the extended error code for other Windows sockets functions as is normally done in Windows Sockets even if 
the <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> function fails or the <b>WSAStartup</b> function was not called to properly initialize Windows Sockets before calling a Windows Sockets function. The <b>WSAGetLastError</b> function is one of the only functions in the Winsock 2.2 DLL that can be called in the case of a <b>WSAStartup</b> failure. </div>
<div> </div>


The Windows Sockets extended error codes returned by this function and the text description of the error are listed under <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>. These error codes and a short text description associated with an error code are defined in the <i>Winerror.h</i> header file. The <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function can be used to obtain the message string for the returned error.

For information on how to handle error codes when porting socket applications to Winsock, see <a href="/windows/desktop/WinSock/error-codes-errno-h-errno-and-wsagetlasterror-2">Error Codes - errno, h_errno and WSAGetLastError</a>. 
		

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/error-codes-errno-h-errno-and-wsagetlasterror-2">Error Codes - errno, h_errno and WSAGetLastError</a>



<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>
