---
UID: NF:winsock.sendto
title: sendto function (winsock.h)
description: The sendto function (winsock.h) sends data to a specific destination.
helpviewer_keywords: ["_win32_sendto_2","sendto","sendto function [Winsock]","winsock.sendto_2","winsock/sendto"]
old-location: winsock\sendto_2.htm
tech.root: WinSock
ms.assetid: a1c89c6b-d11d-4d3e-a664-af2beed0cd09
ms.date: 08/16/2022
ms.keywords: _win32_sendto_2, sendto, sendto function [Winsock], winsock.sendto_2, winsock/sendto
req.header: winsock.h
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
 - sendto
 - winsock/sendto
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
 - sendto
---

# sendto function


## -description

The 
<b>sendto</b> function sends data to a specific destination.

## -parameters

### -param s [in]

A descriptor identifying a (possibly connected) socket.

### -param buf [in]

A pointer to a buffer containing the data to be transmitted.

### -param len [in]

The length, in bytes, of the data pointed to by the <i>buf</i> parameter.

### -param flags [in]

A set of flags that specify the way in which the call is made.

### -param to [in]

An optional pointer to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that contains the address of the target socket.

### -param tolen [in]

The size, in bytes, of the address pointed to by the <i>to</i> parameter.

## -returns

If no error occurs, 
<b>sendto</b> returns the total number of bytes sent, which can be less than the number indicated by <i>len</i>. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The requested address is a broadcast address, but the appropriate flag was not set. Call 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> with the SO_BROADCAST parameter to allow the use of the broadcast address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An unknown flag was specified, or MSG_OOB was specified for a socket with SO_OOBINLINE enabled.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> or <i>to</i> parameters are not part of the user address space, or the <i>tolen</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected (connection-oriented sockets only).

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
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only receive operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to sendto on a socket after 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> has been invoked with <i>how</i> set to SD_SEND or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the requested operation would block.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is message oriented, and the message is larger than the maximum supported by the underlying transport.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEHOSTUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The remote host cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was terminated due to a time-out or other failure. The application should close the socket as it is no longer usable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was reset by the remote side executing a hard or abortive close. For UDP sockets, the remote host was unable to deliver a previously sent UDP datagram and responded with a "Port Unreachable" ICMP packet. The application should close the socket as it is no longer usable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address, for example, ADDR_ANY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEDESTADDRREQ</a></b></dt>
</dl>
</td>
<td width="60%">
A destination address is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEHOSTUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation was attempted to an unreachable host.

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
</table>

## -remarks

The 
<b>sendto</b> function is used to write outgoing data on a socket. For message-oriented sockets, care must be taken not to exceed the maximum packet size of the underlying subnets, which can be obtained by using 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> to retrieve the value of socket option SO_MAX_MSG_SIZE. If the data is too long to pass atomically through the underlying protocol, the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a> is returned and no data is transmitted.

The <i>to</i> parameter can be any valid address in the socket's address family, including a broadcast or any multicast address. To send to a broadcast address, an application must have used 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> with SO_BROADCAST enabled. Otherwise, 
<b>sendto</b> will fail with the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a>. For TCP/IP, an application can send to any multicast address (without becoming a group member).

<div class="alert"><b>Note</b>  If a socket is opened, a 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> call is made, and then a 
<b>sendto</b> call is made, Windows Sockets performs an implicit 
<b>bind</b> function call.</div>
<div> </div>
If the socket is unbound, unique values are assigned to the local association by the system, and the socket is then marked as bound. If the socket is connected, the <a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> function can be used to determine the local IP address and port associated with the socket. 

If the socket is not connected, the  
<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>   function can be used to determine the local port number associated with the socket but the IP address returned is set to the wildcard address for the given protocol (for example, INADDR_ANY  or "0.0.0.0" for IPv4 and IN6ADDR_ANY_INIT or "::" for IPv6).

The successful completion of a 
<b>sendto</b> does not indicate that the data was successfully delivered.

The 
<b>sendto</b> function is normally used on a connectionless socket to send a datagram to a specific peer socket identified by the <i>to</i> parameter. Even if the connectionless socket has been previously connected to a specific address, the <i>to</i> parameter overrides the destination address for that particular datagram only. On a connection-oriented socket, the <i>to</i> and <i>tolen</i> parameters are ignored, making 
<b>sendto</b> equivalent to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>sendto</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>sendto</b> function.


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

    int iResult;
    WSADATA wsaData;

    SOCKET SendSocket = INVALID_SOCKET;
    sockaddr_in RecvAddr;

    unsigned short Port = 27015;

    char SendBuf[1024];
    int BufLen = 1024;

    //----------------------
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }

    //---------------------------------------------
    // Create a socket for sending data
    SendSocket = socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP);
    if (SendSocket == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //---------------------------------------------
    // Set up the RecvAddr structure with the IP address of
    // the receiver (in this example case "192.168.1.1")
    // and the specified port number.
    RecvAddr.sin_family = AF_INET;
    RecvAddr.sin_port = htons(Port);
    RecvAddr.sin_addr.s_addr = inet_addr("192.168.1.1");

    //---------------------------------------------
    // Send a datagram to the receiver
    wprintf(L"Sending a datagram to the receiver...\n");
    iResult = sendto(SendSocket,
                     SendBuf, BufLen, 0, (SOCKADDR *) & RecvAddr, sizeof (RecvAddr));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"sendto failed with error: %d\n", WSAGetLastError());
        closesocket(SendSocket);
        WSACleanup();
        return 1;
    }
    //---------------------------------------------
    // When the application is finished sending, close the socket.
    wprintf(L"Finished sending. Closing socket.\n");
    iResult = closesocket(SendSocket);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"closesocket failed with error: %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //---------------------------------------------
    // Clean up and quit.
    wprintf(L"Exiting.\n");
    WSACleanup();
    return 0;
}


```


<h3><a id="For_Sockets_Using_IP__Version_4_"></a><a id="for_sockets_using_ip__version_4_"></a><a id="FOR_SOCKETS_USING_IP__VERSION_4_"></a>For Sockets Using IP (Version 4)</h3>
To send a broadcast (on a SOCK_DGRAM only), the address pointed to by the <i>to</i> parameter can be constructed to contain the special IPv4 address INADDR_BROADCAST (defined in Winsock2.h), together with the intended port number. If the address pointed to by the <i>to</i> parameter contains the INADDR_BROADCAST address and intended port, then the broadcast will be sent out on all interfaces to that port. 

If the broadcast should be sent out only on a specific interface, then the address pointed to by the <i>to</i> parameter should contain the subnet broadcast address for the interface and the intended port. For example, an IPv4 network address of 192.168.1.0 with a subnet mask of 255.255.255.0 would use a subnet broadcast address of 192.168.1.255. 

It is generally inadvisable for a broadcast datagram to exceed the size at which fragmentation can occur, which implies that the data portion of the datagram (excluding headers) should not exceed 512 bytes.

If no buffer space is available within the transport system to hold the data to be transmitted, 
<b>sendto</b> will block unless the socket has been placed in a nonblocking mode. On nonblocking, stream oriented sockets, the number of bytes written can be between 1 and the requested length, depending on buffer availability on both the client and server systems. The 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>, 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a> function can be used to determine when it is possible to send more data.

Calling 
<b>sendto</b> with a <i>len</i> of zero is permissible and will return zero as a valid value. For message-oriented sockets, a zero-length transport datagram is sent.

The <i>flags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. The semantics of this function are determined by the socket options and the <i>flags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MSG_DONTROUTE</td>
<td>Specifies that the data should not be subject to routing. A Windows Sockets service provider can choose to ignore this flag.</td>
</tr>
<tr>
<td>MSG_OOB</td>
<td>Sends OOB data (stream-style socket such as SOCK_STREAM only). </td>
</tr>
</table>
 

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
