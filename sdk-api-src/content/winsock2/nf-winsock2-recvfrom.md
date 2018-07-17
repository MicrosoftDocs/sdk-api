---
UID: NF:winsock2.recvfrom
title: recvfrom function
author: windows-sdk-content
description: The recvfrom function receives a datagram and stores the source address.
old-location: winsock\recvfrom_2.htm
old-project: winsock
ms.assetid: 3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "_win32_recvfrom_2, recvfrom, recvfrom function [Winsock], winsock.recvfrom_2, winsock/recvfrom"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - recvfrom
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# recvfrom function


## -description


The 
<b>recvfrom</b> function receives a datagram and stores the source address.


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

An optional pointer to a buffer in a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure that will hold the source address upon return.


### -param fromlen [in, out, optional]

An optional pointer to the size, in bytes, of the buffer pointed to by the <i>from</i> parameter.


## -returns



If no error occurs, 
<b>recvfrom</b> returns the number of bytes received. If the connection has been gracefully closed, the return value is zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>buf</i> or <i>from</i> parameters are not in the  user address space, or the <i>fromlen</i> parameter is too small to accommodate the source address of the peer address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) call was canceled through 
<a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound with 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, or an unknown flag was specified, or MSG_OOB was specified for a socket with SO_OOBINLINE enabled, or (for byte stream-style sockets only) <i>len</i> was zero or negative.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is connected. This function is not permitted with a connected socket, whether the socket is connection oriented or connectionless.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor in the <i>s</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only send operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to 
<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a> on a socket after 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">shutdown</a> has been invoked with <i>how</i> set to SD_RECEIVE or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the 
<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a> operation would block.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The message was too large to fit into the buffer pointed to by the <i>buf</i> parameter and was truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been dropped, because of a network failure or because the system on the other end went down without notice.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a></b></dt>
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
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>. Explicit binding is discouraged for client applications. For client applications using this function, the socket can become bound implicitly to a local address through 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>, 
<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>, or 
<a href="https://msdn.microsoft.com/ef9efa03-feed-4f0d-b874-c646cce745c9">WSAJoinLeaf</a>.

For stream-oriented sockets such as those of type SOCK_STREAM, a call to 
<b>recvfrom</b> returns as much information as is currently available—up to the size of the buffer specified. If the socket has been configured for inline reception of OOB data (socket option SO_OOBINLINE) and OOB data is yet unread, only OOB data will be returned. The application can use the 
<a href="https://msdn.microsoft.com/048fcb8d-acd3-4917-a997-dd133db399f8">ioctlsocket</a> or 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a><b>SIOCATMARK</b> command to determine whether any more OOB data remains to be read. The <i>from</i> and <i>fromlen</i> parameters are ignored for connection-oriented sockets.

For message-oriented sockets, data is extracted from the first enqueued message, up to the size of the buffer specified. If the datagram or message is larger than the buffer specified, the buffer is filled with the first part of the datagram, and 
<b>recvfrom</b> generates the error 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEMSGSIZE</a>. For unreliable protocols (for example, UDP) the excess data is lost. For UDP if the packet received contains no data (empty), the return value from the <b>recvfrom</b> function function is zero.

If the <i>from</i> parameter is nonzero and the socket is not connection oriented, (type SOCK_DGRAM for example), the network address of the peer that sent the data is copied to the corresponding 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure. The value pointed to by <i>fromlen</i> is initialized to the size of this structure and is modified, on return, to indicate the actual size of the address stored in the <b>sockaddr</b> structure.

If no incoming data is available at the socket, the 
<b>recvfrom</b> function blocks and waits for data to arrive according to the blocking rules defined for 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> with the MSG_PARTIAL flag not set unless the socket is nonblocking. In this case, a value of SOCKET_ERROR is returned with the error code set to 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a>. The 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>, 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>, or 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> can be used to determine when more data arrives.

If the socket is connection oriented and the remote side has shut down the connection gracefully, the call to 
<b>recvfrom</b> will complete immediately with zero bytes received. If the connection has been reset 
<b>recvfrom</b> will fail with the error 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a>.

The <i>flags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. The semantics of this function are determined by the socket options and the <i>flags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MSG_PEEK</td>
<td>Peeks at the incoming data. The data is copied into the buffer but is not removed from the input queue. The function subsequently returns the amount of data that can be read in a single call to the <b>recvfrom</b> (or <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>) function, which may not be the same as the total amount of data queued on the socket.  The amount of data that can actually be read in a single call to the <b>recvfrom</b> (or <b>recv</b>) function is limited to the data size written in the <a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> or <a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> function call.</td>
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include &lt;winsock2.h&gt;
#include &lt;Ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

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
    iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
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

    iResult = bind(RecvSocket, (SOCKADDR *) &amp; RecvAddr, sizeof (RecvAddr));
    if (iResult != 0) {
        wprintf(L"bind failed with error %d\n", WSAGetLastError());
        return 1;
    }
    //-----------------------------------------------
    // Call the recvfrom function to receive datagrams
    // on the bound socket.
    wprintf(L"Receiving datagrams...\n");
    iResult = recvfrom(RecvSocket,
                       RecvBuf, BufLen, 0, (SOCKADDR *) &amp; SenderAddr, &amp;SenderAddrSize);
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

</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>



<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

