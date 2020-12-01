---
UID: NF:winsock2.WSAEnumNetworkEvents
title: WSAEnumNetworkEvents function (winsock2.h)
description: The WSAEnumNetworkEvents function discovers occurrences of network events for the indicated socket, clear internal network event records, and reset event objects (optional).
helpviewer_keywords: ["WSAEnumNetworkEvents","WSAEnumNetworkEvents function [Winsock]","_win32_wsaenumnetworkevents_2","winsock.wsaenumnetworkevents_2","winsock2/WSAEnumNetworkEvents"]
old-location: winsock\wsaenumnetworkevents_2.htm
tech.root: WinSock
ms.assetid: 2e6abccd-c82c-4a6b-8720-259986ac9984
ms.date: 12/05/2018
ms.keywords: WSAEnumNetworkEvents, WSAEnumNetworkEvents function [Winsock], _win32_wsaenumnetworkevents_2, winsock.wsaenumnetworkevents_2, winsock2/WSAEnumNetworkEvents
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
 - WSAEnumNetworkEvents
 - winsock2/WSAEnumNetworkEvents
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
 - WSAEnumNetworkEvents
---

# WSAEnumNetworkEvents function


## -description

The 
<b>WSAEnumNetworkEvents</b> function discovers occurrences of network events for the indicated socket, clear internal network event records, and reset event objects (optional).

## -parameters

### -param s [in]

A descriptor identifying the socket.

### -param hEventObject [in]

An optional handle identifying an associated event object to be reset.

### -param lpNetworkEvents [out]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanetworkevents">WSANETWORKEVENTS</a> structure that is filled with a record of network events that occurred and any associated error codes.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One of the specified parameters was invalid.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpNetworkEvents</i> parameter is not a valid part of the user address space.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAEnumNetworkEvents</b> function is used to discover which network events have occurred for the indicated socket since the last invocation of this function. It is intended for use in conjunction with 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>, which associates an event object with one or more network events. The recording of network events commences when 
<b>WSAEventSelect</b> is called with a nonzero <i>lNetworkEvents</i> parameter and remains in effect until another call is made to 
<b>WSAEventSelect</b> with the <i>lNetworkEvents</i> parameter set to zero, or until a call is made to 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>.

<b>WSAEnumNetworkEvents</b> only reports network activity and errors nominated through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>. See the descriptions of 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> to find out how those functions report network activity and errors.

The socket's internal record of network events is copied to the structure referenced by <i>lpNetworkEvents</i>, after which the internal network events record is cleared. If the <i>hEventObject</i> parameter is not <b>NULL</b>, the indicated event object is also reset. The Windows Sockets provider guarantees that the operations of copying the network event record, clearing it and resetting any associated event object are atomic, such that the next occurrence of a nominated network event will cause the event object to become set. In the case of this function returning SOCKET_ERROR, the associated event object is not reset and the record of network events is not cleared.

The <b>lNetworkEvents</b> member of the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsanetworkevents">WSANETWORKEVENTS</a> structure indicates which of the FD_XXX network events have occurred. The <b>iErrorCode</b> array is used to contain any associated error codes with the array index corresponding to the position of event bits in <b>lNetworkEvents</b>. Identifiers such as FD_READ_BIT and FD_WRITE_BIT can be used to index the <b>iErrorCode</b> array. Note that only those elements of the <b>iErrorCode</b> array are set that correspond to the bits set in <i>lNetworkEvents</i> parameter. Other parameters are not modified (this is important for backward compatibility with the applications that are not aware of new FD_ROUTING_INTERFACE_CHANGE and FD_ADDRESS_LIST_CHANGE events).

The following error codes can be returned along with the corresponding network event.

<b>Event: FD_CONNECT</b>


<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></td>
<td>Addresses in the specified family cannot be used with this socket.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a></td>
<td>The attempt to connect was forcefully rejected.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></td>
<td>The network cannot be reached from this host at this time.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></td>
<td>No buffer space is available. The socket cannot be connected.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></td>
<td>An attempt to connect timed out without establishing a connection</td>
</tr>
</table>
 



<b>Event: FD_CLOSE</b>


<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></td>
<td>The connection was reset by the remote side.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNABORTED</a></td>
<td>The connection was terminated due to a time-out or other failure.</td>
</tr>
</table>
 



<b>Event: FD_ACCEPT</b>

<b>Event: FD_ADDRESS_LIST_CHANGE</b>

<b>Event: FD_GROUP_QOS</b>

<b>Event: FD_QOS</b>

<b>Event: FD_OOB</b>

<b>Event: FD_READ</b>

<b>Event: FD_WRITE</b>


<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
</table>
 



<b>Event: FD_ROUTING_INTERFACE_CHANGE</b>


<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></td>
<td>The specified destination is no longer reachable.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
</table>
 



<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the WSAEnumNetworkEvents function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <windows.h>

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int main()
{
//-------------------------
// Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    SOCKET SocketArray[WSA_MAXIMUM_WAIT_EVENTS], ListenSocket;
    WSAEVENT EventArray[WSA_MAXIMUM_WAIT_EVENTS];
    WSANETWORKEVENTS NetworkEvents;
    sockaddr_in InetAddr;
    DWORD EventTotal = 0;
    DWORD Index;
    DWORD i;
    
    HANDLE NewEvent = NULL; 

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }

//-------------------------
// Create a listening socket
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"socket function failed with error: %d\n", WSAGetLastError() );
        return 1;
    }
    
    InetAddr.sin_family = AF_INET;
    InetAddr.sin_addr.s_addr = htonl(INADDR_ANY);
    InetAddr.sin_port = htons(27015);

//-------------------------
// Bind the listening socket
    iResult = bind(ListenSocket, (SOCKADDR *) & InetAddr, sizeof (InetAddr));
    if (iResult != 0) {
        wprintf(L"bind failed with error: %d\n", WSAGetLastError() );
        return 1;
    }

//-------------------------
// Create a new event
    NewEvent = WSACreateEvent();
    if (NewEvent == NULL) {
        wprintf(L"WSACreateEvent failed with error: %d\n", GetLastError() );
        return 1;
    }    

//-------------------------
// Associate event types FD_ACCEPT and FD_CLOSE
// with the listening socket and NewEvent
    iResult = WSAEventSelect(ListenSocket, NewEvent, FD_ACCEPT | FD_CLOSE);
    if (iResult != 0) {
        wprintf(L"WSAEventSelect failed with error: %d\n", WSAGetLastError() );
        return 1;
    }

//-------------------------
// Start listening on the socket
    iResult = listen(ListenSocket, 10);
    if (iResult != 0) {
        wprintf(L"listen failed with error: %d\n", WSAGetLastError() );
        return 1;
    }

//-------------------------
// Add the socket and event to the arrays, increment number of events
    SocketArray[EventTotal] = ListenSocket;
    EventArray[EventTotal] = NewEvent;
    EventTotal++;

//-------------------------
// Wait for network events on all sockets
    Index = WSAWaitForMultipleEvents(EventTotal, EventArray, FALSE, WSA_INFINITE, FALSE);
    Index = Index - WSA_WAIT_EVENT_0;

//-------------------------
// Iterate through all events and enumerate
// if the wait does not fail.
    for (i = Index; i < EventTotal; i++) {
        Index = WSAWaitForMultipleEvents(1, &EventArray[i], TRUE, 1000, FALSE);
        if ((Index != WSA_WAIT_FAILED) && (Index != WSA_WAIT_TIMEOUT)) {
            WSAEnumNetworkEvents(SocketArray[i], EventArray[i], &NetworkEvents);
        }
    }

//...
    return 0;


```


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>