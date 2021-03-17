---
UID: NF:winsock2.WSAResetEvent
title: WSAResetEvent function (winsock2.h)
description: The WSAResetEvent function resets the state of the specified event object to nonsignaled.
helpviewer_keywords: ["WSAResetEvent","WSAResetEvent function [Winsock]","_win32_wsaresetevent_2","winsock.wsaresetevent_2","winsock2/WSAResetEvent"]
old-location: winsock\wsaresetevent_2.htm
tech.root: WinSock
ms.assetid: 99a8b0f3-977f-44cd-a224-0819d7513c90
ms.date: 12/05/2018
ms.keywords: WSAResetEvent, WSAResetEvent function [Winsock], _win32_wsaresetevent_2, winsock.wsaresetevent_2, winsock2/WSAResetEvent
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
 - WSAResetEvent
 - winsock2/WSAResetEvent
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
 - WSAResetEvent
---

# WSAResetEvent function


## -description

The 
<b>WSAResetEvent</b> function resets the state of the specified event object to nonsignaled.

## -parameters

### -param hEvent [in]

A handle that identifies an open event object handle.

## -returns

If the 
<b>WSAResetEvent</b> function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
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
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAResetEvent</b> function is used to set the state of the event object to nonsignaled.

The proper way to reset the state of an event object used with the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a> function is to pass the handle of the event object to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnetworkevents">WSAEnumNetworkEvents</a> function in the <i>hEventObject</i> parameter. This will reset the event object and adjust the status of active FD events on the socket in an atomic fashion.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnetworkevents">WSAEnumNetworkEvents</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetevent">WSASetEvent</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>