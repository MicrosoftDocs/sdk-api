---
UID: NF:winsock2.listen
title: listen function (winsock2.h)
description: The listen function places a socket in a state in which it is listening for an incoming connection.
helpviewer_keywords: ["_win32_listen_2","listen","listen function [Winsock]","winsock.listen_2","winsock2/listen"]
old-location: winsock\listen_2.htm
tech.root: WinSock
ms.assetid: 1233feeb-a8c1-49ac-ab34-82af224ecf00
ms.date: 12/05/2018
ms.keywords: _win32_listen_2, listen, listen function [Winsock], winsock.listen_2, winsock2/listen
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
 - listen
 - winsock2/listen
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
 - listen
---

# listen function


## -description

The 
<b>listen</b> function places a socket in a state in which it is listening for an incoming connection.

## -parameters

### -param s [in]

A descriptor identifying a bound, unconnected socket.

### -param backlog [in]

The maximum length of the queue of pending connections. If set to <b>SOMAXCONN</b>, the underlying service provider responsible for socket <i>s</i> will set the backlog to a maximum reasonable value. If set to <b>SOMAXCONN_HINT(N)</b> (where N is a number), the backlog value will be N, adjusted to be within the range (200, 65535). Note that <b>SOMAXCONN_HINT</b> can be used to set the backlog to a larger value than possible with SOMAXCONN.

<b>SOMAXCONN_HINT</b> is only supported by the Microsoft TCP/IP service provider. There is no standard provision to obtain the actual backlog value.

## -returns

If no error occurs, 
<b>listen</b> returns zero. Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs during execution of the 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function, but could be delayed until this function if the 
<b>bind</b> was to a partially wildcard address (involving ADDR_ANY) and if a specific address needs to be committed at the time of this function.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound with 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.

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
The referenced socket is not of a type that supports the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> operation.

</td>
</tr>
</table>

## -remarks

To accept connections, a socket is first created with the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function and bound to a local address with the 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function. A backlog for incoming connections is specified with 
<b>listen</b>, and then the connections are accepted with the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function. Sockets that are connection oriented, those of type <b>SOCK_STREAM</b> for example, are used with 
<b>listen</b>. The socket <i>s</i> is put into passive mode where incoming connection requests are acknowledged and queued pending acceptance by the process.

A value for the <i>backlog</i> of <b>SOMAXCONN</b> is a special constant that  instructs the underlying service provider responsible for socket <i>s</i> to set the length of the queue of pending connections to a maximum reasonable value.

On Windows Sockets 2, this maximum value defaults to a large value (typically several hundred or more). 
 
When calling the <b>listen</b> function in a Bluetooth application, it is strongly recommended that a much lower value be used for the <i>backlog</i> parameter (typically 2 to 4), since only a few client connections are accepted. This reduces the system resources that are allocated for use by the listening socket. This same recommendation applies to other network applications that expect only a few client connections.


The 
<b>listen</b> function is typically used by servers that can have more than one connection request at a time. If a connection request arrives and the queue is full, the client will receive an error with an indication of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a>.

If there are no available socket descriptors, 
<b>listen</b> attempts to continue to function. If descriptors become available, a later call to 
<b>listen</b> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> will refill the queue to the current or most recent value specified for the  <i>backlog</i> parameter, if possible, and resume listening for incoming connections.

If the <b>listen</b> function is called on an already listening socket, it will return success without changing the value for the <i>backlog</i> parameter.  Setting the <i>backlog</i> parameter to 0 in a subsequent call to <b>listen</b> on a listening socket is not considered a proper reset, especially if there are connections on the socket.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>listen</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>listen</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

int wmain()
{

    //----------------------
    // Initialize Winsock
    WSADATA wsaData;
    int iResult = 0;

    SOCKET ListenSocket = INVALID_SOCKET;
    sockaddr_in service;

    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"WSAStartup() failed with error: %d\n", iResult);
        return 1;
    }
    //----------------------
    // Create a SOCKET for listening for incoming connection requests.
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"socket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //----------------------
    // The sockaddr_in structure specifies the address family,
    // IP address, and port for the socket that is being bound.
    service.sin_family = AF_INET;
    service.sin_addr.s_addr = inet_addr("127.0.0.1");
    service.sin_port = htons(27015);

    iResult = bind(ListenSocket, (SOCKADDR *) & service, sizeof (service));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"bind function failed with error %d\n", WSAGetLastError());
        iResult = closesocket(ListenSocket);
        if (iResult == SOCKET_ERROR)
            wprintf(L"closesocket function failed with error %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //----------------------
    // Listen for incoming connection requests 
    // on the created socket
    if (listen(ListenSocket, SOMAXCONN) == SOCKET_ERROR)
        wprintf(L"listen function failed with error: %d\n", WSAGetLastError());

    wprintf(L"Listening on socket...\n");

    iResult = closesocket(ListenSocket);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"closesocket function failed with error %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    WSACleanup();
    return 0;
}

```


<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
For another example that uses the <b>listen</b> function, see <a href="/windows/desktop/WinSock/getting-started-with-winsock">Getting Started With Winsock</a>.

<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>
<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
</ul>
<h3><a id="Compatibility"></a><a id="compatibility"></a><a id="COMPATIBILITY"></a>Compatibility</h3>
The <i>backlog</i> parameter is limited (silently) to a reasonable value as determined by the underlying service provider. Illegal values are replaced by the nearest legal value. There is no standard provision to find out the actual backlog value.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>