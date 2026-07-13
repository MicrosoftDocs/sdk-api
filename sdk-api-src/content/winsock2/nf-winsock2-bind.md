---
UID: NF:winsock2.bind
title: bind function (winsock2.h)
description: The bind function associates a local address with a socket. (bind function (winsock2.h))
helpviewer_keywords: ["_win32_bind_2","bind","bind function [Winsock]","winsock.bind_2","winsock/bind"]
old-location: winsock\bind_2.htm
tech.root: WinSock
ms.assetid: 3a651daa-7404-4ef7-8cff-0d3dff41a8e8
ms.date: 08/03/2022
ms.keywords: _win32_bind_2, bind, bind function [Winsock], winsock.bind_2, winsock/bind
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
 - bind
 - winsock2/bind
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
 - bind
---

# bind function


## -description

The 
<b>bind</b> function associates a local address with a socket.

## -parameters

### -param s [in]

A descriptor identifying an unbound socket.

### -param name [in]

A pointer to a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure of the local address to assign to the bound socket .

### -param namelen [in]

The length, in bytes, of the value pointed to by the <i>name</i> parameter.

## -returns

If no error occurs, 
<b>bind</b> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code can be retrieved by calling 
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
<div class="alert"><b>Note</b>  A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.</div>
<div> </div>
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
An attempt was made to access a socket in a way forbidden by its access permissions.

This error is returned if an attempt to bind a datagram socket to the broadcast address failed because 
the <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> option SO_BROADCAST is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
Only one usage of each socket address (protocol/network address/port) is normally permitted.

This error is returned if a process on the computer is already bound to the same fully qualified address and the socket has not been marked to allow address reuse with SO_REUSEADDR. For example, the IP address and port specified in the <i>name</i> parameter are already bound to another socket being used by another application. For more information, see the SO_REUSEADDR socket option in the <a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET Socket Options</a> reference,  <a href="/windows/desktop/WinSock/using-so-reuseaddr-and-so-exclusiveaddruse">Using SO_REUSEADDR and SO_EXCLUSIVEADDRUSE</a>, and <a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The requested address is not valid in its context.

This error is returned if the specified address pointed to by the <i>name</i> parameter is not a valid local IP address on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid pointer address in attempting to use a pointer argument in a call.

This error is returned if the <i>name</i> parameter is NULL, the <i>name</i> or <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the <i>name</i> parameter contains an incorrect address format for the associated address family, or the first two bytes of the memory block specified by <i>name</i> do not match the address family associated with the socket descriptor <i>s</i>.

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
An invalid argument was supplied.

This error is returned of the socket <i>s</i> is already bound to an address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.

This error is returned of not enough buffers are available or there are too many connections.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
An operation was attempted on something that is not a socket.

This error is returned if the descriptor in the <i>s</i> parameter is not a socket.

</td>
</tr>
</table>

## -remarks

The 
<b>bind</b> function is required on an unconnected socket before subsequent calls to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> function. It is normally used to bind to either connection-oriented (stream) or connectionless (datagram) sockets. The 
<b>bind</b> function may also be used to bind to a raw socket (the socket was created by calling the <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function with the <i>type</i> parameter set to SOCK_RAW). The 
<b>bind</b> function may also be used on an unconnected socket before subsequent calls to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>, or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a> functions before send operations. 

When a socket is created with a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function, it exists in a namespace (address family), but it has no name assigned to it. Use the 
<b>bind</b> function to establish the local association of the socket by assigning a local name to an unnamed socket.


A name consists of three parts when using the Internet address family:

<ul>
<li>The address family.</li>
<li>A host address.</li>
<li>A port number that identifies the application.</li>
</ul>


In Windows Sockets 2, the <i>name</i> parameter is not strictly interpreted as a pointer to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure. It is cast this way for Windows Sockets 1.1 compatibility. Service providers are free to regard it as a pointer to a block of memory of size <i>namelen</i>. The first 2 bytes in this block (corresponding to the <b>sa_family</b> member of the <b>sockaddr</b> structure, the <b>sin_family</b> member of the <b>sockaddr_in</b> structure, or the <b>sin6_family</b> member of the <b>sockaddr_in6</b> structure) must contain the address family that was used to create the socket. Otherwise, an error WSAEFAULT occurs.

If an application does not care what local address is assigned, specify the constant value <b>INADDR_ANY</b> for an IPv4 local address or the constant value <b>in6addr_any</b> for an IPv6 local address in the <b>sa_data</b> member of the <i>name</i> parameter. This allows the underlying service provider to use any appropriate network address, potentially simplifying application programming in the presence of <i>multihomed</i> hosts (that is, hosts that have more than one network interface and address).

For TCP/IP, if the port is specified as zero, the service provider assigns a unique port to the application from the dynamic client port range. On Windows Vista and later, the dynamic client port range is a value between 49152 and 65535. This is a change from Windows Server 2003 and earlier where the dynamic client port range was a value between 1025 and 5000.  The maximum value for the client dynamic port range can be changed by setting a value under  the following registry key:

<b>HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters</b>

The <b>MaxUserPort</b> registry value sets the value to use for the maximum value of the dynamic client port range. You must restart the computer for this setting to take effect.

On Windows Vista and later, the dynamic client port range can be viewed and changed using <b>netsh</b> commands. The dynamic client port range can be set differently for UDP and TCP and also for IPv4 and IPv6. For more information, see <a href="https://support.microsoft.com/kb/929851">KB 929851</a>. 

The application can use 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> after calling 
<b>bind</b> to learn the address and the port that has been assigned to the socket. If the Internet address is equal to <b>INADDR_ANY</b> or <b>in6addr_any</b>, 
<b>getsockname</b> cannot necessarily supply the address until the socket is connected, since several addresses can be valid if the host is multihomed. Binding to a specific port number other than port 0 is discouraged for client applications, since there is a danger of conflicting with another socket already using that port number on the local computer.<div class="alert"><b>Note</b>  When using <b>bind</b> with the SO_EXCLUSIVEADDRUSE or SO_REUSEADDR socket option, the socket option must be set prior to executing <b>bind</b> to have any affect. For more information, see <a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> and <a href="/windows/desktop/WinSock/using-so-reuseaddr-and-so-exclusiveaddruse">Using SO_REUSEADDR and SO_EXCLUSIVEADDRUSE</a>.</div>
<div> </div>


For multicast operations, the preferred method is to call the <b>bind</b> function to associate a socket with a local IP address  and then join the multicast group. Although this order of operations is not mandatory, it is strongly recommended. So a multicast application would first select an IPv4 or IPv6  address on the local computer, the wildcard IPv4 address (<b>INADDR_ANY</b>), or the wildcard IPv6 address (<b>in6addr_any</b>). The multicast application would then call the <b>bind</b> function with this address in the in the <b>sa_data</b> member of the <i>name</i> parameter to associate the local IP address with the socket. If a wildcard address was specified, then Windows will select the local IP address to use. After the <b>bind</b> function completes, an application would then join the multicast group of interest. For more information on how to join a multicast group, see the section on <a href="/windows/desktop/WinSock/multicast-programming">Multicast Programming</a>. This socket can then be used to receive multicast packets from the multicast group using the <a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>, <a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, <a href="/windows/desktop/api/mswsock/nf-mswsock-wsarecvex">WSARecvEx</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, or <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a> functions. 

The <b>bind</b> function is not normally required  for send operations to  a multicast group. The <a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>,<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a>, and  <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> functions implicitly bind the socket to the wildcard address if the socket is not already bound.  The <b>bind</b> function is required before the use of the <a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>  or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> functions which do not perform an implicit bind and are allowed only on connected sockets, which means the socket must have already been bound for it to be connected. The <b>bind</b> function might be used before send operations using the <b>sendto</b>,<b>WSASendMsg</b>, or <b>WSASendTo</b> functions if an application wanted to select a specific local  IP address on a local computer with multiple network interfaces and local IP addresses. Otherwise an implicit bind to the wildcard address using the <b>sendto</b>,<b>WSASendMsg</b> , or <b>WSASendTo</b> functions might result in a different local IP address being used for send operations.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>bind</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>Local names are not exposed in IrDA. IrDA client sockets therefore, must never call the 
<b>bind</b> function before the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function. If the IrDA socket was previously bound to a service name using 
<b>bind</b>, the 
<b>connect</b> function will fail with SOCKET_ERROR.</li>
<li>If the service name is of the form "LSAP-SELxxx," where xxx is a decimal integer in the range 1-127, the address indicates a specific LSAP-SEL xxx rather than a service name. Service names such as these allow server applications to accept incoming connections directed to a specific LSAP-SEL, without first performing an ISA service name query to get the associated LSAP-SEL. One example of this service name type is a non-Windows device that does not support IAS.</li>
</ul>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

The following example demonstrates the use of the <b>bind</b> function. For another example that uses the <b>bind</b> function, see <a href="/windows/desktop/WinSock/getting-started-with-winsock">Getting Started With Winsock</a>.


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

    // Declare some variables
    WSADATA wsaData;

    int iResult = 0;            // used to return function results

    // the listening socket to be created
    SOCKET ListenSocket = INVALID_SOCKET;

    // The socket address to be passed to bind
    sockaddr_in service;

    //----------------------
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"Error at WSAStartup()\n");
        return 1;
    }
    //----------------------
    // Create a SOCKET for listening for 
    // incoming connection requests
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {
        wprintf(L"socket function failed with error: %u\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //----------------------
    // The sockaddr_in structure specifies the address family,
    // IP address, and port for the socket that is being bound.
    service.sin_family = AF_INET;
    service.sin_addr.s_addr = inet_addr("127.0.0.1");
    service.sin_port = htons(27015);

    //----------------------
    // Bind the socket.
    iResult = bind(ListenSocket, (SOCKADDR *) &service, sizeof (service));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"bind failed with error %u\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    else
        wprintf(L"bind returned success\n");

    WSACleanup();
    return 0;
}


```

## -see-also

<a href="/windows/desktop/WinSock/multicast-programming">Multicast Programming</a>



<a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET Socket Options</a>



<a href="/windows/desktop/WinSock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a>



<a href="/windows/desktop/WinSock/tcp-ip-raw-sockets-2">TCP/IP Raw Sockets</a>



<a href="/windows/desktop/WinSock/using-so-reuseaddr-and-so-exclusiveaddruse">Using SO_REUSEADDR and SO_EXCLUSIVEADDRUSE</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
