---
UID: NF:winsock2.WSACloseEvent
title: WSACloseEvent function (winsock2.h)
description: The WSACloseEvent function closes an open event object handle.
helpviewer_keywords: ["WSACloseEvent","WSACloseEvent function [Winsock]","_win32_wsacloseevent_2","winsock.wsacloseevent_2","winsock2/WSACloseEvent"]
old-location: winsock\wsacloseevent_2.htm
tech.root: WinSock
ms.assetid: 40cefe46-10a3-4b6a-8c89-3e16237fc685
ms.date: 12/05/2018
ms.keywords: WSACloseEvent, WSACloseEvent function [Winsock], _win32_wsacloseevent_2, winsock.wsacloseevent_2, winsock2/WSACloseEvent
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
 - WSACloseEvent
 - winsock2/WSACloseEvent
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
 - WSACloseEvent
---

# WSACloseEvent function


## -description

The 
<b>WSACloseEvent</b> function closes an open event object handle.

## -parameters

### -param hEvent [in]

Object handle identifying the open event.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> is not a valid event object handle.

</td>
</tr>
</table>

## -remarks

The 
<b>WSACloseEvent</b> function closes the handle to an event object and frees resources associated with the event object. This function is used to close a handle created by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a> function. Once the handle to the  event object is closed, further references to this handle will fail with the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a>.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnetworkevents">WSAEnumNetworkEvents</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaresetevent">WSAResetEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetevent">WSASetEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>