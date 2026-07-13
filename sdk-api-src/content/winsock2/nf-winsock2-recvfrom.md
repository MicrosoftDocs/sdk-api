---
UID: NF:winsock2.recvfrom
title: recvfrom function (winsock2.h)
description: The recvfrom function receives a datagram, and stores the source address.
helpviewer_keywords: ["_win32_recvfrom_2","recvfrom","recvfrom function [Winsock]","winsock.recvfrom_2","winsock/recvfrom"]
old-location: winsock\recvfrom_2.htm
tech.root: WinSock
ms.assetid: 3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1
ms.date: 12/05/2018
ms.keywords: _win32_recvfrom_2, recvfrom, recvfrom function [Winsock], winsock.recvfrom_2, winsock/recvfrom
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
 - recvfrom
 - winsock2/recvfrom
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
 - recvfrom
---

## -description

The <b>recvfrom</b> function receives a datagram, and stores the source address.

## -parameters

### -param s [in]

A descriptor identifying a bound socket.

### -param buf [out]

A buffer for the incoming data.

### -param len [in]

The length, in bytes, of the buffer pointed to by the <i>buf</i> parameter.

### -param flags [in]

A set of options that modify the behavior of the function call beyond the options specified for the associated socket. See the Remarks below for more details.

### -param from [out]

An optional pointer to a buffer in a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that will hold the source address upon return.

### -param fromlen [in, out, optional]

An optional pointer to the size, in bytes, of the buffer pointed to by the <i>from</i> parameter.

## -returns

If no error occurs, 
<b>recvfrom</b> returns the number of bytes received. If the connection has been gracefully closed, the return value is zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>buf</i> or <i>from</i> parameters are not in the  user address space, or the <i>fromlen</i> parameter is too small to accommodate the source address of the peer address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

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
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, or an unknown flag was specified, or MSG_OOB was specified for a socket with SO_OOBINLINE enabled, or (for byte stream-style sockets only) <i>len</i> was zero or negative.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is connected. This function is not permitted with a connected socket, whether the socket is connection oriented or connectionless.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor in the <i>s</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only send operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> on a socket after 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> has been invoked with <i>how</i> set to SD_RECEIVE or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> operation would block.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The message was too large to fit into the buffer pointed to by the <i>buf</i> parameter and was truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been dropped, because of a network failure or because the system on the other end went down without notice.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was reset by the remote side executing a hard or abortive close. The application should close the socket;  it is no longer usable. On a UDP-datagram socket this error indicates  a previous send operation resulted in an ICMP <i>Port Unreachable</i> message.

</td>
</tr>
</table>

## -remarks

The 
<b>recvfrom</b> function reads incoming data on both connected and unconnected sockets and captures the address from which the data was sent. This function is typically used with connectionless sockets. The local address of the socket must be known. For server applications, this is usually done explicitly through 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>. Explicit binding is discouraged for client applications. For client applications using this function, the socket can become bound implicitly to a local address through 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a>.

For stream-oriented sockets such as those of type SOCK_STREAM, a call to 
<b>recvfrom</b> returns as much information as is currently available—up to the size of the buffer specified. If the socket has been configured for inline reception of OOB data (socket option SO_OOBINLINE) and OOB data is yet unread, only OOB data will be returned. The application can use the 
<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a><b>SIOCATMARK</b> command to determine whether any more OOB data remains to be read. The <i>from</i> and <i>fromlen</i> parameters are ignored for connection-oriented sockets.

For message-oriented sockets, data is extracted from the first enqueued message, up to the size of the buffer specified. If the datagram or message is larger than the buffer specified, the buffer is filled with the first part of the datagram, and 
<b>recvfrom</b> generates the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a>. For unreliable protocols (for example, UDP) the excess data is lost. For UDP if the packet received contains no data (empty), the return value from the <b>recvfrom</b> function is zero.

If the <i>from</i> parameter is nonzero and the socket is not connection oriented, (type SOCK_DGRAM for example), the network address of the peer that sent the data is copied to the corresponding 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure. The value pointed to by <i>fromlen</i> is initialized to the size of this structure and is modified, on return, to indicate the actual size of the address stored in the <b>sockaddr</b> structure.

If no incoming data is available at the socket, the 
<b>recvfrom</b> function blocks and waits for data to arrive according to the blocking rules defined for 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> with the MSG_PARTIAL flag not set unless the socket is nonblocking. In this case, a value of SOCKET_ERROR is returned with the error code set to 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>. The 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>, 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a> can be used to determine when more data arrives.

If the socket is connection oriented and the remote side has shut down the connection gracefully, the call to 
<b>recvfrom</b> will complete immediately with zero bytes received. If the connection has been reset 
<b>recvfrom</b> will fail with the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a>.

The <i>flags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. The semantics of this function are determined by the socket options and the <i>flags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MSG_PEEK</td>
<td>Peeks at the incoming data. The data is copied into the buffer but is not removed from the input queue.</td>
</tr>
<tr>
<td>MSG_OOB</td>
<td>Processes Out Of Band (OOB) data.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>recvfrom</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>recvfrom</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int main()
{

    int iResult = 0;

    WSADATA wsaData;

    SOCKET RecvSocket;
    sockaddr_in RecvAddr;

    unsigned short Port = 27015;

    char RecvBuf[1024];
    int BufLen = 1024;

    sockaddr_in SenderAddr;
    int SenderAddrSize = sizeof (SenderAddr);

    //-----------------------------------------------
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"WSAStartup failed with error %d\n", iResult);
        return 1;
    }
    //-----------------------------------------------
    // Create a receiver socket to receive datagrams
    RecvSocket = socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP);
    if (RecvSocket == INVALID_SOCKET) {
        wprintf(L"socket failed with error %d\n", WSAGetLastError());
        return 1;
    }
    //-----------------------------------------------
    // Bind the socket to any address and the specified port.
    RecvAddr.sin_family = AF_INET;
    RecvAddr.sin_port = htons(Port);
    RecvAddr.sin_addr.s_addr = htonl(INADDR_ANY);

    iResult = bind(RecvSocket, (SOCKADDR *) & RecvAddr, sizeof (RecvAddr));
    if (iResult != 0) {
        wprintf(L"bind failed with error %d\n", WSAGetLastError());
        return 1;
    }
    //-----------------------------------------------
    // Call the recvfrom function to receive datagrams
    // on the bound socket.
    wprintf(L"Receiving datagrams...\n");
    iResult = recvfrom(RecvSocket,
                       RecvBuf, BufLen, 0, (SOCKADDR *) & SenderAddr, &SenderAddrSize);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"recvfrom failed with error %d\n", WSAGetLastError());
    }
 
    //-----------------------------------------------
    // Close the socket when finished receiving datagrams
    wprintf(L"Finished receiving. Closing socket.\n");
    iResult = closesocket(RecvSocket);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"closesocket failed with error %d\n", WSAGetLastError());
        return 1;
    }

    //-----------------------------------------------
    // Clean up and exit.
    wprintf(L"Exiting.\n");
    WSACleanup();
    return 0;
}
```

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>

<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>

<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
