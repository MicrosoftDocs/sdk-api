---
UID: NF:winsock2.WSAAccept
title: WSAAccept function (winsock2.h)
description: The WSAAccept function conditionally accepts a connection based on the return value of a condition function, provides quality of service flow specifications, and allows the transfer of connection data.
helpviewer_keywords: ["WSAAccept","WSAAccept function [Winsock]","_win32_wsaaccept_2","winsock.wsaaccept_2","winsock2/WSAAccept"]
old-location: winsock\wsaaccept_2.htm
tech.root: WinSock
ms.assetid: f385f63f-49b2-4eb7-8717-ad4cca1a2252
ms.date: 12/05/2018
ms.keywords: WSAAccept, WSAAccept function [Winsock], _win32_wsaaccept_2, winsock.wsaaccept_2, winsock2/WSAAccept
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
 - WSAAccept
 - winsock2/WSAAccept
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
 - WSAAccept
---

## -description

The <b>WSAAccept</b> function conditionally accepts a connection based on the return value of a condition function, provides quality of service flow specifications, and allows the transfer of connection data.

## -parameters

### -param s [in]

A descriptor that identifies a socket that is listening for connections after a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> function.

### -param addr [out]

An optional pointer to an <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that receives the address of the connecting entity, as known to the communications layer. The exact format of the <i>addr</i> parameter is determined by the address family established when the socket was created.

### -param addrlen [in, out]

An optional pointer to an integer that contains the length of the <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure pointed to by the <i>addr</i> parameter, in bytes.

### -param lpfnCondition [in]

The  address of an optional, application-specified condition function that will make an accept/reject decision based on the caller information passed in as parameters, and optionally create or join a socket group by assigning an appropriate value to the result parameter <i>g</i> of this function. If this parameter is <b>NULL</b>, then no condition function is called.

### -param dwCallbackData [in]

Callback data passed back to the application-specified condition function as the value of the <i>dwCallbackData</i> parameter passed to the condition function. This parameter is only applicable if the <i>lpfnCondition</i> parameter is not <b>NULL</b>. This parameter is not interpreted by Windows Sockets.

## -returns

If no error occurs, 
<b>WSAAccept</b> returns a value of type SOCKET that is a descriptor for the accepted socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to access a socket in a way forbidden by its access permissions. This error is returned if the connection request that was offered has timed out or been withdrawn.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
No connection could be made because the target machine actively refused it. This error is returned if the connection request was forcefully rejected as indicated in the return value of the condition function (CF_REJECT).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
An existing connection was forcibly closed by the remote host. This error is returned of an incoming connection was indicated, but was subsequently terminated by the remote peer prior to accepting the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned of the <i>addrlen</i> parameter is too small or the <i>addr</i> or <i>lpfnCondition</i> is not part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking operation was interrupted by a call to <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>. This error is returned if a blocking Windows Sockets 1.1 call was canceled through 
<b>WSACancelBlockingCall</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking operation is currently executing. This error is returned if a blocking Windows Sockets 1.1 call is in progress.

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
								This error is returned if <a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> was not invoked prior to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a>, the return value of the condition function is not a valid one, or any case where the specified socket is in an invalid state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
Too many open sockets. This error is returned if the queue is nonempty upon entry to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a> and there are no socket descriptors available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation encountered a dead network. This error is returned if the network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full. This error is returned if no buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
An operation was attempted on something that is not a socket. This error is returned if the socket descriptor passed in the <i>s</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The protocol family has not been configured into the system or no implementation for it exists. This error is returned if the referenced socket is not a type that supports connection-oriented service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
A non-blocking socket operation could not be completed immediately. This error is returned if the socket is marked as nonblocking and no connections are present to be accepted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
Either the application has not called <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>, or <b>WSAStartup</b> failed. This error is returned of a successful 
call to the <b>WSAStartup</b> function dit not occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server. This error is returned if the acceptance of the connection request was deferred as indicated in the return value of the condition function (CF_DEFER).

</td>
</tr>
</table>

## -remarks

The <b>WSAAccept</b> function extracts the first connection on the queue of pending connections on socket <i>s</i>, and checks it against the condition function, provided the condition function is specified (that is, not <b>NULL</b>). If the condition function returns CF_ACCEPT, 
<b>WSAAccept</b> creates a new socket. The newly created socket has the same properties as socket <i>s</i> including asynchronous events registered with 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> or with 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>. If the condition function returns CF_REJECT, 
<b>WSAAccept</b> rejects the connection request. The condition function runs in the same thread as this function does, and should return as soon as possible. If the decision cannot be made immediately, the condition function should return CF_DEFER to indicate that no decision has been made, and no action about this connection request should be taken by the service provider. When the application is ready to take action on the connection request, it will invoke 
<b>WSAAccept</b> again and return either CF_ACCEPT or CF_REJECT as a return value from the condition function.

A socket in default mode (blocking) will block until a connection is present when an application calls 
<b>WSAAccept</b> and no connections are pending on the queue.

A socket in nonblocking mode (blocking) fails with the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> when an application calls 
<b>WSAAccept</b> and no connections are pending on the queue. After 
<b>WSAAccept</b> succeeds and returns a new socket handle, the accepted socket cannot be used to accept any more connections. The original socket remains open and listens for new connection requests.

The <i>addr</i> parameter is a result parameter that is filled in with the address of the connecting entity, as known to the communications layer. The exact format of the <i>addr</i> parameter is determined by the address family in which the communication is occurring. The <i>addrlen</i> is a value-result parameter; it should initially contain the amount of space pointed to by <i>addr</i>. On return, it will contain the actual length (in bytes) of the address returned. This call is used with connection-oriented socket types such as SOCK_STREAM. If <i>addr</i> and/or <i>addrlen</i> are equal to <b>NULL</b>, then no information about the remote address of the accepted socket is returned. Otherwise, these two parameters will be filled in if the connection is successfully accepted.

A prototype of the condition function is defined in the `Winsock2.h` header file as the <b>LPCONDITIONPROC</b>, as follows.

```cpp
int CALLBACK 
ConditionFunc( 
  IN     LPWSABUF    lpCallerId, 
  IN     LPWSABUF    lpCallerData, 
  IN OUT LPQOS       lpSQOS, 
  IN OUT LPQOS       lpGQOS,
  IN     LPWSABUF    lpCalleeId, 
  IN     LPWSABUF    lpCalleeData, 
  OUT    GROUP FAR * g, 	
  IN     DWORD_PTR   dwCallbackData
);
```

The <b>ConditionFunc</b> is a placeholder for the application-specified callback function. The actual condition function must reside in a DLL or application module. It is exported in the module definition file.

The <i>lpCallerId</i> parameter points to a WSABUF structure that contains the address of the connecting entity, where its <i>len</i> parameter is the length of the buffer in bytes, and its <i>buf</i> parameter is a pointer to the buffer. The <i>lpCallerData</i> is a value parameter that contains any user data. The information in these parameters is sent along with the connection request. If no caller identification or caller data is available, the corresponding parameters will be <b>NULL</b>. Many network protocols do not support connect-time caller data. Most conventional network protocols can be expected to support caller identifier information at connection-request time. The buf portion of the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> pointed to by <i>lpCallerId</i> points to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>. The <b>sockaddr</b> structure is interpreted according to its address family (typically by casting the <b>sockaddr</b> to some type specific to the address family).

The <i>lpSQOS</i> parameter references the 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structures for socket <i>s</i> specified by the caller, one for each direction, followed by any additional provider-specific parameters. The sending or receiving flow specification values will be ignored as appropriate for any unidirectional sockets. A <b>NULL</b> value indicates that there is no caller-supplied quality of service and that no negotiation is possible. A non-<b>NULL</b> <i>lpSQOS</i> pointer indicates that a quality of service negotiation is to occur or that the provider is prepared to accept the quality of service request without negotiation.

The <i>lpGQOS</i> parameter is reserved, and should be <b>NULL</b>. (reserved for future use with socket groups) references the 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure for the socket group the caller is to create, one for each direction, followed by any additional provider-specific parameters. A <b>NULL</b> value for <i>lpGQOS</i> indicates no caller-specified group quality of service. Quality of service information can be returned if negotiation is to occur.

The <i>lpCalleeId</i> is a parameter that contains the local address of the connected entity. The <i>buf</i> portion of the WSABUF pointed to by <i>lpCalleeId</i> points to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure. The <b>sockaddr</b> structure is interpreted according to its address family (typically by casting the <b>sockaddr</b> to some type specific to the address family such as struct <b>sockaddr_in</b>).

The <i>lpCalleeData</i> is a result parameter used by the condition function to supply user data back to the connecting entity. The <i>lpCalleeData-&gt;len</i> initially contains the length of the buffer allocated by the service provider and pointed to by <i>lpCalleeData-&gt;buf</i>. A value of zero means passing user data back to the caller is not supported. The condition function should copy up to <i>lpCalleeData-&gt;len</i> bytes of data into <i>lpCalleeData-&gt;buf</i>, and then update <i>lpCalleeData-&gt;len</i> to indicate the actual number of bytes transferred. If no user data is to be passed back to the caller, the condition function should set <i>lpCalleeData-&gt;len</i> to zero. The format of all address and user data is specific to the address family to which the socket belongs.

The <i>g</i> parameter is assigned within the condition function to indicate any of the following actions:

<ul>
<li>If <i>g</i> is an existing socket group identifier, add <i>s</i> to this group, provided all the requirements set by this group are met.</li>
<li>If  <i>g</i> = SG_UNCONSTRAINED_GROUP, create an unconstrained socket group and have <i>s</i> as the first member.</li>
<li>If <i>g</i> = SG_CONSTRAINED_GROUP, create a constrained socket group and have <i>s</i> as the first member.</li>
<li>If <i>g</i> = zero, no group operation is performed.</li>
</ul>
For unconstrained groups, any set of sockets can be grouped together as long as they are supported by a single service provider. A constrained socket group can consist only of connection-oriented sockets, and requires that connections on all grouped sockets be to the same address on the same host. For newly created socket groups, the new group identifier can be retrieved by using 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function with <i>level</i> parameter set to <a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET</a> and the <i>optname</i> parameter set to <b>SO_GROUP_ID</b>.  A socket group and its associated socket group ID remain valid until the last socket belonging to this socket group is closed. Socket group IDs are unique across all processes for a given service provider. A socket group and its associated identifier remain valid until the last socket belonging to this socket group is closed. Socket group identifiers are unique across all processes for a given service provider. For more information on socket groups, see the Remarks for the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> functions.

The <i>dwCallbackData</i> parameter value passed to the condition function is the value passed as the <i>dwCallbackData</i> parameter in the original 
<b>WSAAccept</b> call. This value is interpreted only by the Windows Socket version 2 client. This allows a client to pass some context information from the 
<b>WSAAccept</b> call site through to the condition function. This also provides the condition function with any additional information required to determine whether to accept the connection or not. A typical usage is to pass a (suitably cast) pointer to a data structure containing references to application-defined objects with which this socket is associated.

<div class="alert"><b>Note</b>  To protect use of the <b>WSAAccept</b> function from SYN attacks, applications must perform full TCP handshakes (SYN-SYNACK-ACK) before reporting the connection request. Protecting against SYN attacks in this manner results in the SO_CONDITIONAL_ACCEPT socket option becoming inoperative; the conditional function is still called, and the <b>WSAAccept</b> function operates properly, but   server applications that rely on clients being unable to perform the handshake will not operate properly.</div>
<div> </div>
<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSAAccept</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>WSAAccept</b> function.

```cpp
#include <winsock2.h>
#include <stdio.h>
#include <windows.h>

/* Define an example conditional function that depends on the pQos field */
int CALLBACK ConditionAcceptFunc(
    LPWSABUF lpCallerId,
    LPWSABUF lpCallerData,
    LPQOS pQos,
    LPQOS lpGQOS,
    LPWSABUF lpCalleeId,
    LPWSABUF lpCalleeData,
    GROUP FAR * g,
    DWORD_PTR dwCallbackData
    )
{

    if (pQos != NULL) {
        RtlZeroMemory(pQos, sizeof(QOS));
        return CF_ACCEPT;
    } else
        return CF_REJECT;
}

int main() {

    /* Declare and initialize variables */
    WSADATA wsaData;
    SOCKET ListenSocket, AcceptSocket;
    struct sockaddr_in saClient;
    int iClientSize = sizeof(saClient);
    u_short port = 27015;
    char* ip;
    sockaddr_in service;
    int error;

    /* Initialize Winsock */
    error = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (error) {
        printf("WSAStartup() failed with error: %d\n", error);
        return 1;
    }

    /* Create a TCP listening socket */
    ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ListenSocket == INVALID_SOCKET) {  
        printf("socket() failed with error: %d\n", WSAGetLastError() );
        WSACleanup();
        return 1;
    }

    /*-----------------------------------------  
     *  Set up the sock addr structure that the listening socket
     *  will be bound to. In this case, the structure holds the
     * local IP address and the port specified. */
    service.sin_family = AF_INET;
    service.sin_port = htons(port);
    hostent* thisHost;
    thisHost = gethostbyname("");
    ip = inet_ntoa (*(struct in_addr *)*thisHost->h_addr_list);
    service.sin_addr.s_addr = inet_addr(ip);

    /*-----------------------------------------
     *  Bind the listening socket to the IP address.
     * and port number specified by the sockaddr structure. */
    error = bind(ListenSocket, (SOCKADDR *) &service, sizeof(SOCKADDR));
    if (error == SOCKET_ERROR) {  
        printf("bind() failed with error: %d\n", WSAGetLastError() );
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
  
    /* Make the socket listen for incoming connection requests */
    error = listen(ListenSocket, 1);
    if (error == SOCKET_ERROR) {  
        printf("listen() failed with error: %d\n", WSAGetLastError() );
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
    printf("Listening...\n");
  
    /*-----------------------------------------
     *  Accept an incoming connection request on the
     *  listening socket and transfer control to the 
     * accepting socket. */
    AcceptSocket = WSAAccept(ListenSocket, (SOCKADDR*) &saClient, &iClientSize, 
        &ConditionAcceptFunc, NULL);
 
    /*  Now do some work with the AcceptSocket 
     *  At this point, the application could
     *  handle data transfer on the socket, or other socket
     * functionality.*/
    
    /* Then clean up and quit */

    closesocket(AcceptSocket);
    closesocket(ListenSocket);
    WSACleanup();

    return 0;
}
```

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>

<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>

<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>

<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>

<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>

<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>