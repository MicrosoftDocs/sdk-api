---
UID: NF:winsock2.WSACreateEvent
title: WSACreateEvent function (winsock2.h)
description: The WSACreateEvent function creates a new event object.
helpviewer_keywords: ["WSACreateEvent","WSACreateEvent function [Winsock]","_win32_wsacreateevent_2","winsock.wsacreateevent_2","winsock2/WSACreateEvent"]
old-location: winsock\wsacreateevent_2.htm
tech.root: WinSock
ms.assetid: cff3bc31-f34c-4bb2-9004-5ec31d0a704a
ms.date: 12/05/2018
ms.keywords: WSACreateEvent, WSACreateEvent function [Winsock], _win32_wsacreateevent_2, winsock.wsacreateevent_2, winsock2/WSACreateEvent
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
 - WSACreateEvent
 - winsock2/WSACreateEvent
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
 - WSACreateEvent
---

# WSACreateEvent function


## -description

The 
<b>WSACreateEvent</b> function creates a new event object.



## -returns

If no error occurs, 
<b>WSACreateEvent</b> returns the handle of the event object. Otherwise, the return value is WSA_INVALID_EVENT. To get extended error information, call 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
Not enough free memory available to create the event object.

</td>
</tr>
</table>

## -remarks

The 
<b>WSACreateEvent</b> function creates a manual-reset event object with an initial state of nonsignaled. The handle of the event object returned cannot be inherited by child processes. 
The event object is unnamed.

The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasetevent">WSASetEvent</a> function can be called to set the state of the event object to signaled. The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaresetevent">WSAResetEvent</a> function can be called to set the state of the event object to nonsignaled. When an event object is no longer needed, the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a> function should be called to free the resources associated with the event object.

Windows Sockets 2 event objects are system objects in Windows environments. Therefore, if a Windows application wants to use an auto-reset event rather than a manual-reset event, the application can call the <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function directly. The scope of an event object is limited to the process in which it is created.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>



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
