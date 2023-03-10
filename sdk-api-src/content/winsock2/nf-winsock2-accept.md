---
UID: NF:winsock2.accept
title: accept function (winsock2.h)
description: The accept function permits an incoming connection attempt on a socket.
helpviewer_keywords: ["_win32_accept_2","accept","accept function [Winsock]","winsock.accept_2","winsock2/accept"]
old-location: winsock\accept_2.htm
tech.root: WinSock
ms.assetid: 72246263-4806-4ab2-9b26-89a1782a954b
ms.date: 12/05/2018
ms.keywords: _win32_accept_2, accept, accept function [Winsock], winsock.accept_2, winsock2/accept
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
 - accept
 - winsock2/accept
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
 - accept
---

# accept function


## -description

The 
<b>accept</b> function permits an incoming connection attempt on a socket.

## -parameters

### -param s [in]

A descriptor that identifies a socket that has been placed in a listening state with the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> function. The connection is actually made with the socket that is returned by 
<b>accept</b>.

### -param addr [out]

An optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer. The exact format of the <i>addr</i> parameter is determined by the address family that was established when the socket from the 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure was created.

### -param addrlen [in, out]

An optional pointer to an integer that contains the length of structure pointed to by the <i>addr</i> parameter.

## -returns

If no error occurs, 
<b>accept</b> returns a value of type <b>SOCKET</b> that is a descriptor for the new socket. This returned value is a handle for the socket on which the actual connection is made.

Otherwise, a value of <b>INVALID_SOCKET</b> is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

The integer referred to by <i>addrlen</i> initially contains the amount of space pointed to by <i>addr</i>. On return it will contain the actual length in bytes of the address returned.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
An incoming connection was indicated, but was subsequently terminated by the remote peer prior to accepting the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>addrlen</i> parameter is too small or <i>addr</i> is not a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> function was not invoked prior to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
The queue is nonempty upon entry to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> and there are no descriptors available.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The referenced socket is not a type that supports connection-oriented service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and no connections are present to be accepted.

</td>
</tr>
</table>

## -remarks

The 
<b>accept</b> function extracts the first connection on the queue of pending connections on socket <i>s</i>. It then creates and returns a handle to the new socket. The newly created socket is the socket that will handle the actual connection; it has the same properties as socket <i>s</i>, including the asynchronous events registered with the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a> functions.

The 
<b>accept</b> function can block the caller until a connection is present if no pending connections are present on the queue, and the socket is marked as blocking. If the socket is marked as nonblocking and no pending connections are present on the queue, 
<b>accept</b> returns an error as described in the following. After the successful completion of 
<b>accept</b> returns a new socket handle, the accepted socket cannot be used to accept more connections. The original socket remains open and listens for new connection requests.

The parameter <i>addr</i> is a result parameter that is filled in with the address of the connecting entity, as known to the communications layer. The exact format of the <i>addr</i> parameter is determined by the address family in which the communication is occurring. The <i>addrlen</i> is a value-result parameter; it should initially contain the amount of space pointed to by <i>addr</i>; on return it will contain the actual length (in bytes) of the address returned.

The 
<b>accept</b> function is used with connection-oriented socket types such as SOCK_STREAM. If <i>addr</i> and/or <i>addrlen</i> are equal to <b>NULL</b>, then no information about the remote address of the accepted socket is returned.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>accept</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>accept</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <winsock2.h>
#include <WS2tcpip.h>
#include <stdio.h>
#include <windows.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int wmain(void)
{

    //----------------------
    // Initialize Winsock.
    WSADATA wsaData;
    int iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"WSAStartup failed with error: %ld\n", iResult);
        return 1;
    }
    //----------------------
    // Create a SOCKET for listening for
    // incoming connection requests.
    SOCKET ListenSocket;
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //----------------------
    // The sockaddr_in structure specifies the address family,
    // IP address, and port for the socket that is being bound.
    sockaddr_in service;
    service.sin_family = AF_INET;
    service.sin_port = htons(27015);
    inet_pton(AF_INET, "127.0.0.1", &service.sin_addr);

    if (bind(ListenSocket,
             (SOCKADDR *) & service, sizeof (service)) == SOCKET_ERROR) {
        wprintf(L"bind failed with error: %ld\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    //----------------------
    // Listen for incoming connection requests.
    // on the created socket
    if (listen(ListenSocket, 1) == SOCKET_ERROR) {
        wprintf(L"listen failed with error: %ld\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    //----------------------
    // Create a SOCKET for accepting incoming requests.
    SOCKET AcceptSocket;
    wprintf(L"Waiting for client to connect...\n");

    //----------------------
    // Accept the connection.
    AcceptSocket = accept(ListenSocket, NULL, NULL);
    if (AcceptSocket == INVALID_SOCKET) {
        wprintf(L"accept failed with error: %ld\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    } else
        wprintf(L"Client connected.\n");

    // No longer need server socket
    closesocket(ListenSocket);

    WSACleanup();
    return 0;
}


```


For another example that uses the  <b>accept</b> function, see <a href="/windows/desktop/WinSock/getting-started-with-winsock">Getting Started With Winsock</a>.

<h3><a id="Notes_for_ATM"></a><a id="notes_for_atm"></a><a id="NOTES_FOR_ATM"></a>Notes for ATM</h3>

The following are important issues associated with connection setup, and must be considered when using Asynchronous Transfer Mode (ATM) with Windows Sockets 2:

<ul>
<li>The 
<b>accept</b> and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a> functions do not necessarily set the remote address and address length parameters. Therefore, when using ATM, the caller should use the 
<b>WSAAccept</b> function and place ATM_CALLING_PARTY_NUMBER_IE in the 
<b>ProviderSpecific</b> member of the 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QoS</a> structure, which itself is included in the <i>lpSQOS</i> parameter of the callback function used in accordance with 
<b>WSAAccept</b>.</li>
<li>When using the 
<b>accept</b> function, realize that the function may return before connection establishment has traversed the entire distance between sender and receiver. This is because the 
<b>accept</b> function returns as soon as it receives a CONNECT ACK message; in ATM, a CONNECT ACK message is returned by the next switch in the path as soon as a CONNECT message is processed (rather than the CONNECT ACK being sent by the end node to which the connection is ultimately established). As such, applications should realize that if data is sent immediately following receipt of a CONNECT ACK message, data loss is possible, since the connection may not have been established all the way between sender and receiver.</li>
</ul>


<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
