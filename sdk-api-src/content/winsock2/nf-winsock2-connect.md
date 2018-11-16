---
UID: NF:winsock2.connect
title: connect function
author: windows-sdk-content
description: The connect function establishes a connection to a specified socket.
old-location: winsock\connect_2.htm
tech.root: WinSock
ms.assetid: 13468139-dc03-45bd-850c-7ac2dbcb6e60
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_connect_2, connect, connect function [Winsock], winsock.connect_2, winsock2/connect"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - connect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- connect
: 
---

# connect function


## -description


The 
<b>connect</b> function establishes a connection to a specified socket.


## -parameters




### -param s [in]

A descriptor identifying an unconnected socket.


### -param name [in]

A pointer to the 
<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure to which the connection should be established.


### -param namelen [in]

The length, in bytes, of the <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure pointed to by the <i>name</i> parameter.


## -returns



If no error occurs, 
<b>connect</b> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

On a blocking socket, the return value indicates success or failure of the connection attempt.


With a nonblocking socket, the connection attempt cannot be completed immediately. In this case, 
<b>connect</b> will return SOCKET_ERROR, and 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> will return 
<a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a>. In this case, there are three possible scenarios:

<ul>
<li>Use the 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> function to determine the completion of the connection request by checking to see if the socket is writeable.</li>
<li>If the application is using 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> to indicate interest in connection events, then the application will receive an FD_CONNECT notification indicating that the 
<b>connect</b> operation is complete (successfully or not).</li>
<li>If the application is using 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> to indicate interest in connection events, then the associated event object will be signaled indicating that the 
<b>connect</b> operation is complete (successfully or not).</li>
</ul>


Until the connection attempt completes on a nonblocking socket, all subsequent calls to 
<b>connect</b> on the same socket will fail with the error code 
<a href="windows_sockets_error_codes_2.htm">WSAEALREADY</a>, and 
<a href="windows_sockets_error_codes_2.htm">WSAEISCONN</a> when the connection completes successfully. Due to ambiguities in version 1.1 of the Windows Sockets specification, error codes returned from 
<b>connect</b> while a connection is already pending may vary among implementations. As a result, it is not recommended that applications use multiple calls to connect to detect connection completion. If they do, they must be prepared to handle 
<a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a> and 
<a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a> error values the same way that they handle 
<a href="windows_sockets_error_codes_2.htm">WSAEALREADY</a>, to assure robust operation.

If the error code returned indicates the connection attempt failed (that is, 
<a href="windows_sockets_error_codes_2.htm">WSAECONNREFUSED</a>, 
<a href="windows_sockets_error_codes_2.htm">WSAENETUNREACH</a>, 
<a href="windows_sockets_error_codes_2.htm">WSAETIMEDOUT</a>) the application can call 
<b>connect</b> again for the same socket.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs when executing 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, but could be delayed until the <a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> function if the 
<b>bind</b> was to a wildcard address (<b>INADDR_ANY</b> or <b>in6addr_any</b>) for the local IP address. A specific address needs to be implicitly bound by the <b>connect</b>  function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The blocking Windows Socket 1.1 call was canceled through 
<a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonblocking 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> call is in progress on the specified socket.


<div class="alert"><b>Note</b>  In order to preserve backward compatibility, this error is reported as 
<a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a> to Windows Sockets 1.1 applications that link to either Winsock.dll or Wsock32.dll.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address (such as <b>INADDR_ANY</b> or <b>in6addr_any</b>) .

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to connect was forcefully rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure pointed to by the <i>name</i> contains incorrect address format for the associated address family  or the <i>namelen</i> parameter is too small. This error is also returned if the <b>sockaddr</b> structure pointed to by the <i>name</i> parameter with a length  specified in the <i>namelen</i> parameter is not in a valid part of the user address space. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>s</i> is a listening socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already connected (connection-oriented sockets only).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEHOSTUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation was attempted to an unreachable host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  No buffer space is available. The socket cannot be connected.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor specified in the <i>s</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
An attempt to connect timed out without establishing a connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the connection cannot be completed immediately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
An attempt to connect a datagram socket to broadcast address failed because 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> option SO_BROADCAST is not enabled.

</td>
</tr>
</table>
 




## -remarks



The 
<b>connect</b> function is used to create a connection to the specified destination. If socket <i>s</i>, is unbound, unique values are assigned to the local association by the system, and the socket is marked as bound.

For connection-oriented sockets (for example, type SOCK_STREAM), an active connection is initiated to the foreign host using <i>name</i> (an address in the namespace of the socket; for a detailed description, see 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> and 
<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a>).<div class="alert"><b>Note</b>  If a socket is opened, a 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> call is made, and then a 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function call.</div>
<div> </div>


When the socket call completes successfully, the socket is ready to send and receive data. If the address member of the structure specified by the <i>name</i> parameter is filled with zeros, 
<b>connect</b> will return the error 
<a href="windows_sockets_error_codes_2.htm">WSAEADDRNOTAVAIL</a>. Any attempt to reconnect an active connection will fail with the error code 
<a href="windows_sockets_error_codes_2.htm">WSAEISCONN</a>.

For connection-oriented, nonblocking sockets, it is often not possible to complete the connection immediately. In such a case, this function returns the error 
<a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a>. However, the operation proceeds.


When the success or failure outcome becomes known, it may be reported in one of two ways, depending on how the client registers for notification.

<ul>
<li>If the client uses the 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> function, success is reported in the writefds set and failure is reported in the exceptfds set.</li>
<li>If the client uses the functions 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure.</li>
</ul>


For a connectionless socket (for example, type SOCK_DGRAM), the operation performed by 
<b>connect</b> is merely to establish a default destination address that can be used on subsequent 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>/
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a> and 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>/
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> calls. Any datagrams received from an address other than the destination address specified will be discarded. If the address member of the structure specified by <i>name</i> is filled with zeros, the socket will be disconnected. Then, the default remote address will be indeterminate, so 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>/
				<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a> and 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>/
				<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> calls will return the error code 
<a href="windows_sockets_error_codes_2.htm">WSAENOTCONN</a>. However, 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>/
				<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a> and 
<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>/
				<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a> can still be used. The default destination can be changed by simply calling 
<b>connect</b> again, even if the socket is already connected. Any datagrams queued for receipt are discarded if <i>name</i> is different from the previous 
<b>connect</b>.

For connectionless sockets, <i>name</i> can indicate any valid address, including a broadcast address. However, to connect to a broadcast address, a socket must use 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> to enable the SO_BROADCAST option. Otherwise, 
<b>connect</b> will fail with the error code 
<a href="windows_sockets_error_codes_2.htm">WSAEACCES</a>.

When a connection between sockets is broken, the socket that was connected should be discarded and new socket should be created. When a problem develops on a connected socket, the application must discard the socket and create the socket again in order to return to a stable point.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>connect</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>connect</b> function.

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
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

int wmain()
{
    //----------------------
    // Initialize Winsock
    WSADATA wsaData;
    int iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"WSAStartup function failed with error: %d\n", iResult);
        return 1;
    }
    //----------------------
    // Create a SOCKET for connecting to server
    SOCKET ConnectSocket;
    ConnectSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ConnectSocket == INVALID_SOCKET) {
        wprintf(L"socket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //----------------------
    // The sockaddr_in structure specifies the address family,
    // IP address, and port of the server to be connected to.
    sockaddr_in clientService;
    clientService.sin_family = AF_INET;
    clientService.sin_addr.s_addr = inet_addr("127.0.0.1");
    clientService.sin_port = htons(27015);

    //----------------------
    // Connect to server.
    iResult = connect(ConnectSocket, (SOCKADDR *) &amp; clientService, sizeof (clientService));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"connect function failed with error: %ld\n", WSAGetLastError());
        iResult = closesocket(ConnectSocket);
        if (iResult == SOCKET_ERROR)
            wprintf(L"closesocket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    wprintf(L"Connected to server.\n");

    iResult = closesocket(ConnectSocket);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"closesocket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    WSACleanup();
    return 0;
}

</pre>
</td>
</tr>
</table></span></div>
For another example that uses the <b>connect</b> function, see <a href="https://msdn.microsoft.com/905cd5bc-44af-4d3f-841a-9e9a2700a785">Getting Started With Winsock</a>.

<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>If an existing IrDA connection is detected at the media-access level, 
<a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a> is returned.</li>
<li>If active connections to a device with a different address exist, 
<a href="windows_sockets_error_codes_2.htm">WSAEADDRINUSE</a> is returned.</li>
<li>If the socket is already connected or an exclusive/multiplexed mode change failed, 
<a href="windows_sockets_error_codes_2.htm">WSAEISCONN</a> is returned.</li>
<li>If the socket was previously bound to a local service name to accept incoming connections using 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, 
<a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a> is returned. Note that once a socket is bound, it cannot be used for establishing an outbound connection.</li>
</ul>


IrDA implements the connect function with addresses of the form sockaddr_irda. Typically, a client application will create a socket with the socket function, scan the immediate vicinity for IrDA devices with the IRLMP_ENUMDEVICES socket option, choose a device from the returned list, form an address, and then call 
<b>connect</b>. There is no difference between blocking and nonblocking semantics.




## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/be20a731-cdfc-48ae-90b2-43f2cf9ecf6d">getsockname</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>



<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

