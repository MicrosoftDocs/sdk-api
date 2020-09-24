---
UID: NF:winsock2.WSALookupServiceEnd
title: WSALookupServiceEnd function (winsock2.h)
description: The WSALookupServiceEnd function is called to free the handle after previous calls to WSALookupServiceBegin and WSALookupServiceNext.
helpviewer_keywords: ["WSALookupServiceEnd","WSALookupServiceEnd function [Winsock]","_win32_wsalookupserviceend_2","winsock.wsalookupserviceend_2","winsock2/WSALookupServiceEnd"]
old-location: winsock\wsalookupserviceend_2.htm
tech.root: WinSock
ms.assetid: f9d2ac54-a818-464d-918e-80ebb5b1b106
ms.date: 12/05/2018
ms.keywords: WSALookupServiceEnd, WSALookupServiceEnd function [Winsock], _win32_wsalookupserviceend_2, winsock.wsalookupserviceend_2, winsock2/WSALookupServiceEnd
req.header: winsock2.h
req.include-header: 
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
 - WSALookupServiceEnd
 - winsock2/WSALookupServiceEnd
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
 - WSALookupServiceEnd
---

# WSALookupServiceEnd function


## -description

The 
<b>WSALookupServiceEnd</b> function is called to free the handle after previous calls to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>.
			

If you call 
<b>WSALookupServiceEnd</b> from another thread while an existing 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> is blocked, the end call will have the same effect as a cancel and will cause the 
<b>WSALookupServiceNext</b> call to return immediately.

## -parameters

### -param hLookup [in]

Handle previously obtained by calling 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>.

## -returns

The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>

## -remarks

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-wsalookupserviceend">Bluetooth and WSALookupServiceEnd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>