---
UID: NF:winsock2.WSAAsyncSelect
title: WSAAsyncSelect function (winsock2.h)
description: The WSAAsyncSelect function (winsock2.h) requests Windows message based notification of network events for a socket. 
helpviewer_keywords: ["WSAAsyncSelect","WSAAsyncSelect function [Winsock]","_win32_wsaasyncselect_2","winsock.wsaasyncselect_2","winsock/WSAAsyncSelect"]
old-location: winsock\wsaasyncselect_2.htm
tech.root: WinSock
ms.assetid: a4d3f599-358c-4a94-91eb-7e1c80244250
ms.date: 08/03/2022
ms.keywords: WSAAsyncSelect, WSAAsyncSelect function [Winsock], _win32_wsaasyncselect_2, winsock.wsaasyncselect_2, winsock/WSAAsyncSelect
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - WSAAsyncSelect
 - winsock2/WSAAsyncSelect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
 - wsock32.dll
api_name:
 - WSAAsyncSelect
---

# WSAAsyncSelect function


## -description

<p class="CCE_Message">[The <b>WSAAsyncSelect</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Rather than use Select-style I/O, use <a href="/windows/desktop/WinSock/overlapped-i-o-and-event-objects-2">Overlapped I/O and Event Objects</a> with WinSock2.]

The 
<b>WSAAsyncSelect</b> function requests Windows message-based notification of network events for a socket.

## -parameters

### -param s [in]

A descriptor that identifies the socket for which event notification is required.

### -param hWnd [in]

A handle that identifies the window that will receive a message when a network event occurs.

### -param wMsg [in]

A message to be received when a network event occurs.

### -param lEvent [in]

A bitmask that specifies a combination of network events in which the application is interested.

## -returns

If the 
<b>WSAAsyncSelect</b> function succeeds, the return value is zero, provided that the application's declaration of interest in the network event set was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
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
The network subsystem failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One of the specified parameters was invalid, such as the window handle not referring to an existing window, or the specified socket is in an invalid state.

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
</table>
 

Additional error codes can be set when an application window receives a message. This error code is extracted from the <i>lParam</i> in the reply message using the <b>WSAGETSELECTERROR</b> macro. Possible error codes for each network event are listed in the following table.

Event: FD_CONNECT

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
<td>The attempt to connect was rejected.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></td>
<td>The network cannot be reached from this host at this time.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></td>
<td>The <i>namelen</i> parameter is invalid.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></td>
<td>The socket is already bound to an address.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></td>
<td>The socket is already connected.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></td>
<td>No more file descriptors are available.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></td>
<td>No buffer space is available. The socket cannot be connected.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></td>
<td>The socket is not connected.</td>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></td>
<td>Attempt to connect timed out without establishing a connection.</td>
</tr>
</table>
 

Event: FD_CLOSE

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem failed.</td>
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
 

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></td>
<td>The network subsystem failed.</td>
</tr>
</table>
 

Event: FD_ROUTING_INTERFACE_CHANGE

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
<td>The network subsystem failed.</td>
</tr>
</table>

## -remarks

The 
<b>WSAAsyncSelect</b> function is used to request that WS2_32.DLL should send a message to the window <i>hWnd</i> when it detects any network event specified by the <i>lEvent</i> parameter. The message that should be sent is specified by the <i>wMsg</i> parameter. The socket for which notification is required is identified by the <i>s</i> parameter.

The <b>WSAAsyncSelect</b> function automatically sets socket <i>s</i> to nonblocking mode, regardless of the value of <i>lEvent</i>. To set socket <i>s</i> back to blocking mode, it is first necessary to clear the event record associated with socket <i>s</i> via a call to <b>WSAAsyncSelect</b> with <i>lEvent</i> set to zero. You can then call <a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a> or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> to set the socket back to blocking mode.  For more information about how to set the nonblocking socket back to blocking mode, see the <b>ioctlsocket</b> and <b>WSAIoctl</b> functions.

The <i>lEvent</i> parameter is constructed by using the bitwise OR operator with any value listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>FD_READ</b></td>
<td>Set to receive notification of readiness for reading.</td>
</tr>
<tr>
<td><b>FD_WRITE</b></td>
<td>Wants to receive notification of readiness for writing.</td>
</tr>
<tr>
<td><b>FD_OOB</b></td>
<td>Wants to receive notification of the arrival of OOB data.</td>
</tr>
<tr>
<td><b>FD_ACCEPT</b></td>
<td>Wants to receive notification of incoming connections.</td>
</tr>
<tr>
<td><b>FD_CONNECT</b></td>
<td>Wants to receive notification of completed connection or multipoint join operation.</td>
</tr>
<tr>
<td><b>FD_CLOSE</b></td>
<td>Wants to receive notification of socket closure.</td>
</tr>
<tr>
<td><b>FD_QOS</b></td>
<td>Wants to receive notification of socket Quality of Service (QoS) changes.</td>
</tr>
<tr>
<td><b>FD_GROUP_QOS</b></td>
<td>Wants to receive notification of socket group Quality of Service (QoS) changes (reserved for future use with socket groups). Reserved.</td>
</tr>
<tr>
<td><b>FD_ROUTING_INTERFACE_CHANGE</b></td>
<td>Wants to receive notification of routing interface changes for the specified destination(s).</td>
</tr>
<tr>
<td><b>FD_ADDRESS_LIST_CHANGE</b></td>
<td>Wants to receive notification of local address list changes for the socket protocol family.</td>
</tr>
</table>
 

Issuing a 
<b>WSAAsyncSelect</b> for a socket cancels any previous 
<b>WSAAsyncSelect</b> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a> for the same socket. For example, to receive notification for both reading and writing, the application must call 
<b>WSAAsyncSelect</b> with both <b>FD_READ</b> and <b>FD_WRITE</b>, as follows:


```cpp
rc = WSAAsyncSelect(s, hWnd, wMsg, FD_READ|FD_WRITE);

```


It is not possible to specify different messages for different events. The following code will not work; the second call will cancel the effects of the first, and only <b>FD_WRITE</b> events will be reported with message wMsg2:


```cpp
rc = WSAAsyncSelect(s, hWnd, wMsg1, FD_READ);
rc = WSAAsyncSelect(s, hWnd, wMsg2, FD_WRITE);

```


To cancel all notification indicating that Windows Sockets should send no further messages related to network events on the socket, <i>lEvent</i> is set to zero.


```cpp
rc = WSAAsyncSelect(s, hWnd, 0, 0);

```


Although 
<b>WSAAsyncSelect</b> immediately disables event message posting for the socket in this instance, it is possible that messages could be waiting in the application message queue. Therefore, the application must be prepared to receive network event messages even after cancellation. Closing a socket with 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> also cancels 
<b>WSAAsyncSelect</b> message sending, but the same caveat about messages in the queue still applies.

The socket created by the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function has the same properties as the listening socket used to accept it. Consequently, 
<b>WSAAsyncSelect</b> events set for the listening socket also apply to the accepted socket. For example, if a listening socket has 
<b>WSAAsyncSelect</b> events <b>FD_ACCEPT</b>, <b>FD_READ</b>, and <b>FD_WRITE</b>, then any socket accepted on that listening socket will also have <b>FD_ACCEPT</b>, <b>FD_READ</b>, and <b>FD_WRITE</b> events with the same <i>wMsg</i> value used for messages. If a different <i>wMsg</i> or events are desired, the application should call 
<b>WSAAsyncSelect</b>, passing the accepted socket and the desired new data.

When one of the nominated network events occurs on the specified socket <i>s</i>, the application window <i>hWnd</i> receives message <i>wMsg</i>. The <i>wParam</i> parameter identifies the socket on which a network event has occurred. The low word of <i>lParam</i> specifies the network event that has occurred. The high word of <i>lParam</i> contains any error code. The error code be any error as defined in Winsock2.h.

<div class="alert"><b>Note</b>  Upon receipt of an event notification message, the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function cannot be used to check the error value because the error value returned can differ from the value in the high word of <i>lParam</i>.</div>
<div> </div>
The error and event codes can be extracted from the <i>lParam</i> using the macros <b>WSAGETSELECTERROR</b> and <b>WSAGETSELECTEVENT</b>, defined in Winsock2.h as:


```cpp
#include <windows.h>

#define WSAGETSELECTEVENT(lParam)       LOWORD(lParam)
#define WSAGETSELECTERROR(lParam)       HIWORD(lParam)

```


The use of these macros will maximize the portability of the source code for the application.

The possible network event codes that can be returned are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>FD_READ</b></td>
<td>Socket <i>s</i> ready for reading.</td>
</tr>
<tr>
<td><b>FD_WRITE</b></td>
<td>Socket <i>s</i> ready for writing.</td>
</tr>
<tr>
<td><b>FD_OOB</b></td>
<td>OOB data ready for reading on socket <i>s</i></td>
</tr>
<tr>
<td><b>FD_ACCEPT</b></td>
<td>Socket <i>s</i> ready for accepting a new incoming connection.</td>
</tr>
<tr>
<td><b>FD_CONNECT</b></td>
<td>Connection or multipoint <i>join</i> operation initiated on socket <i>s</i> completed.</td>
</tr>
<tr>
<td><b>FD_CLOSE</b></td>
<td>Connection identified by socket <i>s</i> has been closed.</td>
</tr>
<tr>
<td><b>FD_QOS</b></td>
<td>Quality of Service associated with socket <i>s</i> has changed.</td>
</tr>
<tr>
<td><b>FD_GROUP_QOS</b></td>
<td>Reserved. Quality of Service associated with the socket group to which <i>s</i> belongs has changed (reserved for future use with socket groups).</td>
</tr>
<tr>
<td><b>FD_ROUTING_INTERFACE_CHANGE</b></td>
<td>Local interface that should be used to send to the specified destination has changed.</td>
</tr>
<tr>
<td><b>FD_ADDRESS_LIST_CHANGE</b></td>
<td>The list of addresses of the socket protocol family to which the application client can bind has changed.</td>
</tr>
</table>
 

Although 
<b>WSAAsyncSelect</b> can be called with interest in multiple events, the application window will receive a single message for each network event.

As in the case of the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function, 
<b>WSAAsyncSelect</b> will frequently be used to determine when a data transfer operation (<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> or 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>) can be issued with the expectation of immediate success. Nevertheless, a robust application must be prepared for the possibility that it can receive a message and issue a Windows Sockets 2 call that returns 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> immediately. For example, the following sequence of events is possible:

<ol>
<li>Data arrives on socket <i>s</i>; Windows Sockets 2 posts 
<b>WSAAsyncSelect</b> message</li>
<li>Application processes some other message</li>
<li>While processing, application issues an <code>ioctlsocket(s, FIONREAD...)</code> and notices that there is data ready to be read</li>
<li>Application issues a <code>recv(s,...)</code> to read the data</li>
<li>Application loops to process next message, eventually reaching the 
<b>WSAAsyncSelect</b> message indicating that data is ready to read</li>
<li>Application issues <code>recv(s,...)</code>, which fails with the error <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>.</li>
</ol>
Other sequences are also possible.

The WS2_32.DLL will not continually flood an application with messages for a particular network event. Having successfully posted notification of a particular event to an application window, no further message(s) for that network event will be posted to the application window until the application makes the function call that implicitly reenables notification of that network event.

<table>
<tr>
<th>Event</th>
<th>Reenabling function</th>
</tr>
<tr>
<td><b>FD_READ</b></td>
<td>
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>, 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>.</td>
</tr>
<tr>
<td><b>FD_WRITE</b></td>
<td>
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>, 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>.</td>
</tr>
<tr>
<td><b>FD_OOB</b></td>
<td>
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>, 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>.</td>
</tr>
<tr>
<td><b>FD_ACCEPT</b></td>
<td>
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a> unless the error code is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a> indicating that the condition function returned CF_DEFER.</td>
</tr>
<tr>
<td><b>FD_CONNECT</b></td>
<td>None.</td>
</tr>
<tr>
<td><b>FD_CLOSE</b></td>
<td>None.</td>
</tr>
<tr>
<td><b>FD_QOS</b></td>
<td>
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with command SIO_GET_QOS.</td>
</tr>
<tr>
<td><b>FD_GROUP_QOS</b></td>
<td>Reserved.
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with command SIO_GET_GROUP_QOS (reserved for future use with socket groups).</td>
</tr>
<tr>
<td><b>FD_ROUTING_INTERFACE_CHANGE</b></td>
<td>
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with command SIO_ROUTING_INTERFACE_CHANGE.</td>
</tr>
<tr>
<td><b>FD_ADDRESS_LIST_CHANGE</b></td>
<td>
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with command SIO_ADDRESS_LIST_CHANGE.</td>
</tr>
</table>
 

Any call to the reenabling routine, even one that fails, results in reenabling of message posting for the relevant event.

For <b>FD_READ</b>, <b>FD_OOB</b>, and <b>FD_ACCEPT</b> events, message posting is level-triggered. This means that if the reenabling routine is called and the relevant condition is still met after the call, a 
<b>WSAAsyncSelect</b> message is posted to the application. This allows an application to be event-driven and not be concerned with the amount of data that arrives at any one time. Consider the following sequence:

<ol>
<li>Network transport stack receives 100 bytes of data on socket <i>s</i> and causes Windows Sockets 2 to post an <b>FD_READ</b> message.</li>
<li>The application issues 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>( <i>s</i>, <i>buffptr</i>, 50, 0) to read 50 bytes.</li>
<li>Another <b>FD_READ</b> message is posted because there is still data to be read.</li>
</ol>
With these semantics, an application need not read all available data in response to an <b>FD_READ</b> message—a single 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> in response to each <b>FD_READ</b> message is appropriate. If an application issues multiple 
<b>recv</b> calls in response to a single <b>FD_READ</b>, it can receive multiple <b>FD_READ</b> messages. Such an application can require disabling <b>FD_READ</b> messages before starting the 
<b>recv</b> calls by calling 
<b>WSAAsyncSelect</b> with the <b>FD_READ</b> event not set.

The <b>FD_QOS</b> and <b>FD_GROUP_QOS</b> events are considered edge triggered. A message will be posted exactly once when a quality of service change occurs. Further messages will not be forthcoming until either the provider detects a further change in quality of service or the application renegotiates the quality of service for the socket.

The <b>FD_ROUTING_INTERFACE_CHANGE</b> message is posted when the local interface that should be used to reach the destination specified in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with SIO_ROUTING_INTERFACE_CHANGE changes after such IOCTL has been issued.

The <b>FD_ADDRESS_LIST_CHANGE</b> message is posted when the list of addresses to which the application can bind changes after 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with SIO_ADDRESS_LIST_CHANGE has been issued.

If any event has occurred when the application calls 
<b>WSAAsyncSelect</b> or when the reenabling function is called, then a message is posted as appropriate. For example, consider the following sequence:

<ol>
<li>An application calls 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>.</li>
<li>A connect request is received, but not yet accepted.</li>
<li>The application calls 
<b>WSAAsyncSelect</b> specifying that it requires receiving <b>FD_ACCEPT</b> messages for the socket. Due to the persistence of events, Windows Sockets 2 posts an <b>FD_ACCEPT</b> message immediately.</li>
</ol>
The <b>FD_WRITE</b> event is handled slightly differently. An <b>FD_WRITE</b> message is posted when a socket is first connected with 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> (after FD_CONNECT, if also registered) or accepted with 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a>, and then after a send operation fails with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> and buffer space becomes available. Therefore, an application can assume that sends are possible starting from the first <b>FD_WRITE</b> message and lasting until a send returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>. After such a failure the application will be notified that sends are again possible with an <b>FD_WRITE</b> message.

The <b>FD_OOB</b> event is used only when a socket is configured to receive OOB data separately. If the socket is configured to receive OOB data inline, the OOB (expedited) data is treated as normal data and the application should register an interest in, and will receive, <b>FD_READ</b> events, not <b>FD_OOB</b> events. An application can set or inspect the way in which OOB data is to be handled by using 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> or 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> for the SO_OOBINLINE option.

The error code in an <b>FD_CLOSE</b> message indicates whether the socket close was graceful or abortive. If the error code is zero, then the close was graceful; if the error code is 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a>, then the socket's virtual circuit was reset. This only applies to connection-oriented sockets such as SOCK_STREAM.

The <b>FD_CLOSE</b> message is posted when a close indication is received for the virtual circuit corresponding to the socket. In TCP terms, this means that the <b>FD_CLOSE</b> is posted when the connection goes into the TIME WAIT or CLOSE WAIT states. This results from the remote end performing a 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> on the send side or a 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>. <b>FD_CLOSE</b> should only be posted after all data is read from a socket, but an application should check for remaining data upon receipt of <b>FD_CLOSE</b> to avoid any possibility of losing data.

Be aware that the application will only receive an <b>FD_CLOSE</b> message to indicate closure of a virtual circuit, and only when all the received data has been read if this is a graceful close. It will not receive an <b>FD_READ</b> message to indicate this condition.

The <b>FD_QOS</b> or <b>FD_GROUP_QOS</b> message is posted when any parameter in the flow specification associated with socket <i>s</i> or the socket group that <i>s</i> belongs to has changed, respectively. Applications should use 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with command SIO_GET_QOS or SIO_GET_GROUP_QOS to get the current quality of service for socket <i>s</i> or for the socket group <i>s</i> belongs to, respectively.

The <b>FD_ROUTING_INTERFACE_CHANGE</b> and <b>FD_ADDRESS_LIST_CHANGE</b> events are considered edge triggered as well. A message will be posted exactly once when a change occurs after the application has requested the notification by issuing 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with SIO_ROUTING_INTERFACE_CHANGE or SIO_ADDRESS_LIST_CHANGE correspondingly. Further messages will not be forthcoming until the application reissues the IOCTL and another change is detected because the IOCTL has been issued.

Here is a summary of events and conditions for each asynchronous notification message.

<ul>
<li><b>FD_READ</b>: 


<ol>
<li>When 
<b>WSAAsyncSelect</b> is called, if there is data currently available to receive.</li>
<li>When data arrives, if <b>FD_READ</b> is not already posted.</li>
<li>After 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> or 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> is called, with or without MSG_PEEK), if data is still available to receive. 


<div class="alert"><b>Note</b>  When 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> SO_OOBINLINE is enabled, data includes both normal data and OOB data in the instances noted above.</div>
<div> </div>
</li>
</ol>
</li>
<li><b>FD_WRITE</b>: 


<ol>
<li>When 
<b>WSAAsyncSelect</b> called, if a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> or 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> is possible.</li>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> called, when connection established.</li>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> or 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> fail with 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>, when 
<b>send</b> or 
<b>sendto</b> are likely to succeed.</li>
<li>After 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> on a connectionless socket. <b>FD_WRITE</b> may or may not occur at this time (implementation-dependent). In any case, a connectionless socket is always writable immediately after a 
<b>bind</b> operation.</li>
</ol>
</li>
<li><b>FD_OOB</b>: Only valid when 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> SO_OOBINLINE is disabled (default). 


<ol>
<li>When 
<b>WSAAsyncSelect</b> called, if there is OOB data currently available to receive with the MSG_OOB flag.</li>
<li>When OOB data arrives, if <b>FD_OOB</b> not already posted.</li>
<li>After 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> or 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> called with or without MSG_OOB flag, if OOB data is still available to receive.</li>
</ol>
</li>
<li><b>FD_ACCEPT</b>: 


<ol>
<li>When 
<b>WSAAsyncSelect</b> called, if there is currently a connection request available to accept.</li>
<li>When a connection request arrives, if <b>FD_ACCEPT</b> not already posted.</li>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> called, if there is another connection request available to accept.</li>
</ol>
</li>
<li><b>FD_CONNECT</b>: 


<ol>
<li>When 
<b>WSAAsyncSelect</b> called, if there is currently a connection established.</li>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> called, when connection is established, even when 
<b>connect</b> succeeds immediately, as is typical with a datagram socket.</li>
<li>After calling 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a>, when join operation completes.</li>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a> was called with a nonblocking, connection-oriented socket. The initial operation returned with a specific error of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>, but the network operation went ahead. Whether the operation eventually succeeds or not, when the outcome has been determined, <b>FD_CONNECT</b> happens. The client should check the error code to determine whether the outcome was successful or failed.</li>
</ol>
</li>
<li><b>FD_CLOSE</b>: Only valid on connection-oriented sockets (for example, SOCK_STREAM) 


<ol>
<li>When 
<b>WSAAsyncSelect</b> called, if socket connection has been closed.</li>
<li>After remote system initiated graceful close, when no data currently available to receive (Be aware that, if data has been received and is waiting to be read when the remote system initiates a graceful close, the <b>FD_CLOSE</b> is not delivered until all pending data has been read).</li>
<li>After local system initiates graceful close with 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> and remote system has responded with "End of Data" notification (for example, TCP FIN), when no data currently available to receive.</li>
<li>When remote system terminates connection (for example, sent TCP RST), and <i>lParam</i> will contain 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a> error value. 


<div class="alert"><b>Note</b>  <b>FD_CLOSE</b> is not posted after 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> is called.</div>
<div> </div>
</li>
</ol>
</li>
<li><b>FD_QOS</b>: 


<ol>
<li>When 
<b>WSAAsyncSelect</b> called, if the quality of service associated with the socket has been changed.</li>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with SIO_GET_QOS called, when the quality of service is changed.</li>
</ol>
</li>
<li><b>FD_GROUP_QOS</b>: Reserved.</li>
<li><b>FD_ROUTING_INTERFACE_CHANGE</b>: 


<ul>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with SIO_ROUTING_INTERFACE_CHANGE called, when the local interface that should be used to reach the destination specified in the IOCTL changes.</li>
</ul>
</li>
<li><b>FD_ADDRESS_LIST_CHANGE</b>: 


<ul>
<li>After 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with SIO_ADDRESS_LIST_CHANGE called, when the list of local addresses to which the application can bind changes.</li>
</ul>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>
