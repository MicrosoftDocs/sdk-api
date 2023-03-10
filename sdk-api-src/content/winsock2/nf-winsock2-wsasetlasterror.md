---
UID: NF:winsock2.WSASetLastError
title: WSASetLastError function (winsock2.h)
description: The WSASetLastError function (winsock2.h) sets the error code that can be retrieved through the WSAGetLastError function. 
helpviewer_keywords: ["WSASetLastError","WSASetLastError function [Winsock]","_win32_wsasetlasterror_2","winsock.wsasetlasterror_2","winsock/WSASetLastError"]
old-location: winsock\wsasetlasterror_2.htm
tech.root: WinSock
ms.assetid: 596155ee-3dcc-4ae3-97ab-0653e019cbee
ms.date: 08/03/2022
ms.keywords: WSASetLastError, WSASetLastError function [Winsock], _win32_wsasetlasterror_2, winsock.wsasetlasterror_2, winsock/WSASetLastError
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
 - WSASetLastError
 - winsock2/WSASetLastError
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
 - WSASetLastError
---

# WSASetLastError function


## -description

The 
<b>WSASetLastError</b> function sets the error code that can be retrieved through the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function.

## -parameters

### -param iError [in]

Integer that specifies the error code to be returned by a subsequent 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> call.

## -returns

This function generates no return values.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
</table>

## -remarks

The 
<b>WSASetLastError</b> function allows an application to set the error code to be returned by a subsequent 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> call for the current thread. Note that any subsequent Windows Sockets routine called by the application will override the error code as set by this routine.

The error code set by 
<b>WSASetLastError</b> is different from the error code reset by calling the function 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> with SO_ERROR. 

The Windows Sockets error codes used by this function are listed under <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>
