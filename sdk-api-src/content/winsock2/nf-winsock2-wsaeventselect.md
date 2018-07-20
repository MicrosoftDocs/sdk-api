---
UID: NF:winsock2.WSAEventSelect
title: WSAEventSelect function
author: windows-sdk-content
description: The WSAEventSelect function specifies an event object to be associated with the specified set of FD_XXX network events.
old-location: winsock\wsaeventselect_2.htm
old-project: winsock
ms.assetid: f98a71e4-47fb-47a4-b37e-e4cc801a8f98
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: WSAEventSelect, WSAEventSelect function [Winsock], _win32_wsaeventselect_2, winsock.wsaeventselect_2, winsock2/WSAEventSelect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WSAEventSelect
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAEventSelect function


## -description



			The 
<b>WSAEventSelect</b> function specifies an event object to be associated with the specified set of FD_XXX network events.


## -parameters




### -param s [in]

A descriptor identifying the socket.


### -param hEventObject [in]

A handle identifying the event object to be associated with the specified set of FD_XXX network events.


### -param lNetworkEvents [in]

A bitmask that specifies the combination of FD_XXX network events in which the application has interest.


## -returns




						The return value is zero if the application's specification of the network events and the associated event object was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

As in the case of the 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> and 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> functions, 
<b>WSAEventSelect</b> will frequently be used to determine when a data transfer operation (<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> or 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>) can be issued with the expectation of immediate success. Nevertheless, a robust application must be prepared for the possibility that the event object is set and it issues a Windows Sockets call that returns 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a> immediately. For example, the following sequence of operations is possible:

<ul>
<li>Data arrives on socket <i>s</i>; Windows Sockets sets the 
<b>WSAEventSelect</b> event object.</li>
<li>The application does some other processing.</li>
<li>While processing, the application issues an 
<a href="https://msdn.microsoft.com/048fcb8d-acd3-4917-a997-dd133db399f8">ioctlsocket</a>(<i>s</i>, FIONREAD...) and notices that there is data ready to be read.</li>
<li>The application issues a 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>(<i>s</i>,...) to read the data.</li>
<li>The application eventually waits on the event object specified in 
<b>WSAEventSelect</b>, which returns immediately indicating that data is ready to read.</li>
<li>The application issues 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>(<i>s</i>,...), which fails with the error 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a>.</li>
</ul>
Having successfully recorded the occurrence of the network event (by setting the corresponding bit in the internal network event record) and signaled the associated event object, no further actions are taken for that network event until the application makes the function call that implicitly reenables the setting of that network event and signaling of the associated event object.

<table>
<tr>
<th>Network event</th>
<th>Re-enabling function</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_READ</b></dt>
</dl>
</td>
<td width="60%">

								The <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>, 
<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>, 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>, <a href="https://msdn.microsoft.com/0ed639f7-e7bd-49a2-a7c0-177699a2cf5e">WSARecvEx</a>, or 
<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_WRITE</b></dt>
</dl>
</td>
<td width="60%">

								The <a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>, 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>, 
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>, or 
<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_OOB</b></dt>
</dl>
</td>
<td width="60%">
The 
								<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>, 
<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>, 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>, <a href="https://msdn.microsoft.com/0ed639f7-e7bd-49a2-a7c0-177699a2cf5e">WSARecvEx</a>, or <a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_ACCEPT</b></dt>
</dl>
</td>
<td width="60%">
The 
								<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>, <a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>, or 
<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a> function unless the error code returned is WSATRY_AGAIN indicating that the condition function returned CF_DEFER.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
None.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
None.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_QOS</b></dt>
</dl>
</td>
<td width="60%">
The 
								<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with command <b>SIO_GET_QOS</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_GROUP_QOS</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_ROUTING_
INTERFACE_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The 
								<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with command <b>SIO_ROUTING_INTERFACE_CHANGE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FD_ADDRESS_
LIST_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The 
								<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with command <b>SIO_ADDRESS_LIST_CHANGE</b>.

</td>
</tr>
</table>
 

Any call to the reenabling routine, even one that fails, results in reenabling of recording and signaling for the relevant network event and event object.

For FD_READ, FD_OOB, and FD_ACCEPT network events, network event recording and event object signaling are level-triggered. This means that if the reenabling routine is called and the relevant network condition is still valid after the call, the network event is recorded and the associated event object is set. This allows an application to be event-driven and not be concerned with the amount of data that arrives at any one time. Consider the following sequence:

<ol>
<li>The transport provider receives 100 bytes of data on socket <i>s</i> and causes WS2_32.DLL to record the FD_READ network event and set the associated event object.</li>
<li>The application issues <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>(<i>s</i>, <i>buffptr</i>, 50, 0) to read 50 bytes.</li>
<li>The transport provider causes WS2_32.DLL to record the FD_READ network event and sets the associated event object again since there is still data to be read.</li>
</ol>
With these semantics, an application need not read all available data in response to an FD_READ network event—a single 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> in response to each FD_READ network event is appropriate.

The FD_QOS event is considered edge triggered. A message will be posted exactly once when a quality of service change occurs. Further messages will not be forthcoming until either the provider detects a further change in quality of service or the application renegotiates the quality of service for the socket.

The FD_ROUTING_INTERFACE_CHANGE and FD_ADDRESS_LIST_CHANGE events are considered edge triggered as well. A message will be posted exactly once when a change occurs after the application has requested the notification by issuing 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with <b>SIO_ROUTING_INTERFACE_CHANGE</b> or <b>SIO_ADDRESS_LIST_CHANGE</b> correspondingly. Other messages will not be forthcoming until the application reissues the IOCTL and another change is detected since the IOCTL has been issued.

If a network event has already happened when the application calls 
<b>WSAEventSelect</b> or when the reenabling function is called, then a network event is recorded and the associated event object is set as appropriate. For example, consider the following sequence:

<ol>
<li>An application calls 
<a href="https://msdn.microsoft.com/1233feeb-a8c1-49ac-ab34-82af224ecf00">listen</a>.</li>
<li>A connect request is received but not yet accepted.</li>
<li>The application calls 
<b>WSAEventSelect</b> specifying that it is interested in the FD_ACCEPT network event for the socket. Due to the persistence of network events, Windows Sockets records the FD_ACCEPT network event and sets the associated event object immediately.</li>
</ol>
The FD_WRITE network event is handled slightly differently. An FD_WRITE network event is recorded when a socket is first connected with a call to the  
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, <a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>, <a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>, <a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a>, or  <a href="https://msdn.microsoft.com/6d87699f-03bd-4579-9907-ae3c29b7332b">WSAConnectByName</a> function or when a socket is accepted with 
<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>, <a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>,
							or <a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a> function and then after a send fails with <a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a> and buffer space becomes available. Therefore, an application can assume that sends are possible starting from the first FD_WRITE network event setting and lasting until a send returns 
WSAEWOULDBLOCK. After such a failure the application will find out that sends are again possible when an FD_WRITE network event is recorded and the associated event object is set.

The FD_OOB network event is used only when a socket is configured to receive OOB data separately. If the socket is configured to receive OOB data inline, the OOB (expedited) data is treated as normal data and the application should register an interest in, and will get FD_READ network event, not FD_OOB network event. An application can set or inspect the way in which OOB data is to be handled by using 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> or 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> for the SO_OOBINLINE option.

The error code in an FD_CLOSE network event indicates whether the socket close was graceful or abortive. If the error code is zero, then the close was graceful; if the error code is 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a>, then the socket's virtual circuit was reset. This only applies to connection-oriented sockets such as SOCK_STREAM.

The FD_CLOSE network event is recorded when a close indication is received for the virtual circuit corresponding to the socket. In TCP terms, this means that the FD_CLOSE is recorded when the connection goes into the TIME WAIT or CLOSE WAIT states. This results from the remote end performing a 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">shutdown</a> on the send side or a 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>. FD_CLOSE being posted after all data is read from a socket. An application should check for remaining data upon receipt of FD_CLOSE to avoid any possibility of losing data. For more information, see the section on <a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Graceful Shutdown, Linger Options, and Socket Closure</a> and the <b>shutdown</b> function.

Note that Windows Sockets will record only an FD_CLOSE network event to indicate closure of a virtual circuit. It will not record an FD_READ network event to indicate this condition.

The FD_QOS or FD_GROUP_QOS network event is recorded when any parameter in the flow specification associated with socket <i>s</i>. Applications should use 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with command <b>SIO_GET_QOS</b> to get the current quality of service for socket <i>s</i>.

The FD_ROUTING_INTERFACE_CHANGE network event is recorded when the local interface that should be used to reach the destination specified in 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with <b>SIO_ROUTING_INTERFACE_CHANGE</b> changes after such IOCTL has been issued.

The FD_ADDRESS_LIST_CHANGE network event is recorded when the list of addresses of protocol family for the socket to which the application can bind changes after 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with <b>SIO_ADDRESS_LIST_CHANGE</b> has been issued.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></td>
<td>A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></td>
<td>The network subsystem has failed.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></td>
<td>One of the specified parameters was invalid, or the specified socket is in an invalid state.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></td>
<td>A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></td>
<td>The descriptor is not a socket.</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAEventSelect</b> function is used to specify an event object, <i>hEventObject</i>, to be associated with the selected FD_XXX network events, <i>lNetworkEvents</i>. The socket for which an event object is specified is identified by the <i>s</i> parameter. The event object is set when any of the nominated network events occur.

The 
<b>WSAEventSelect</b> function operates very similarly to 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>, the difference being the actions taken when a nominated network event occurs. The 
<b>WSAAsyncSelect</b> function causes an application-specified Windows message to be posted. The 
<b>WSAEventSelect</b> sets the associated event object and records the occurrence of this event in an internal network event record. An application can use 
<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a> to wait or poll on the event object, and use 
<a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a> to retrieve the contents of the internal network event record and thus determine which of the nominated network events have occurred.

The proper way to reset the state of an event object used with the <b>WSAEventSelect</b> function is to pass the handle of the event object to the <a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a> function in the <i>hEventObject</i> parameter. This will reset the event object and adjust the status of active FD events on the socket in an atomic fashion.

<b>WSAEventSelect</b> is the only function that causes network activity and errors to be recorded and retrievable through 
<a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a>. See the descriptions of 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> and 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> to find out how those functions report network activity and errors.

The <b>WSAEventSelect</b> function automatically sets socket <i>s</i> to nonblocking mode, regardless of the value of <i>lNetworkEvents</i>. To set socket <i>s</i> back to blocking mode, it is first necessary to clear the event record associated with socket <i>s</i> via a call to <b>WSAEventSelect</b> with <i>lNetworkEvents</i> set to zero and the <i>hEventObject</i> parameter set to <b>NULL</b>. You can then call <a href="https://msdn.microsoft.com/048fcb8d-acd3-4917-a997-dd133db399f8">ioctlsocket</a> or <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> to set the socket back to blocking mode.

The <i>lNetworkEvents</i> parameter is constructed by using the bitwise OR operator with any of the values specified in the following list.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>FD_READ</td>
<td>Wants to receive notification of readiness for reading.</td>
</tr>
<tr>
<td>FD_WRITE</td>
<td>Wants to receive notification of readiness for writing.</td>
</tr>
<tr>
<td>FD_OOB</td>
<td>Wants to receive notification of the arrival of OOB data.</td>
</tr>
<tr>
<td>FD_ACCEPT</td>
<td>Wants to receive notification of incoming connections.</td>
</tr>
<tr>
<td>FD_CONNECT</td>
<td>Wants to receive notification of completed connection or multipoint join operation.</td>
</tr>
<tr>
<td>FD_CLOSE</td>
<td>Wants to receive notification of socket closure.</td>
</tr>
<tr>
<td>FD_QOS</td>
<td>Wants to receive notification of socket (QoS changes.</td>
</tr>
<tr>
<td>FD_GROUP_QOS</td>
<td>Reserved for future use with socket groups. Want to receive notification of socket group QoS changes.</td>
</tr>
<tr>
<td>FD_ROUTING_
INTERFACE_CHANGE</td>
<td>Wants to receive notification of routing interface changes for the specified destination.</td>
</tr>
<tr>
<td>FD_ADDRESS_
LIST_CHANGE</td>
<td>Wants to receive notification of local address list changes for the address family of the socket.</td>
</tr>
</table>
 



Issuing a 
<b>WSAEventSelect</b> for a socket cancels any previous 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or 
<b>WSAEventSelect</b> for the same socket and clears the internal network event record. For example, to associate an event object with both reading and writing network events, the application must call 
<b>WSAEventSelect</b> with both FD_READ and FD_WRITE, as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>rc = WSAEventSelect(s, hEventObject, FD_READ|FD_WRITE);
</pre>
</td>
</tr>
</table></span></div>
It is not possible to specify different event objects for different network events. The following code will not work; the second call will cancel the effects of the first, and only the FD_WRITE network event will be associated with <i>hEventObject2</i>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>rc = WSAEventSelect(s, hEventObject1, FD_READ);
rc = WSAEventSelect(s, hEventObject2, FD_WRITE); //bad
</pre>
</td>
</tr>
</table></span></div>
To cancel the association and selection of network events on a socket, <i>lNetworkEvents</i> should be set to zero, in which case the <i>hEventObject</i> parameter will be ignored.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>rc = WSAEventSelect(s, hEventObject, 0);
</pre>
</td>
</tr>
</table></span></div>
Closing a socket with 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> also cancels the association and selection of network events specified in 
<b>WSAEventSelect</b> for the socket. The application, however, still must call 
<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a> to explicitly close the event object and free any resources.

The socket created when the 
<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> function is called has the same properties as the listening socket used to accept it. Any 
<b>WSAEventSelect</b> association and network events selection set for the listening socket apply to the accepted socket. For example, if a listening socket has 
<b>WSAEventSelect</b> association of <i>hEventObject</i> with FD_ACCEPT, FD_READ, and FD_WRITE, then any socket accepted on that listening socket will also have FD_ACCEPT, FD_READ, and FD_WRITE network events associated with the same <i>hEventObject</i>. If a different <i>hEventObject</i> or network events are desired, the application should call 
<b>WSAEventSelect</b>, passing the accepted socket and the desired new information.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>WSAEventSelect</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//-------------------------
// Declare and initialize variables
SOCKET ListenSocket;
WSAEVENT NewEvent;
sockaddr_in InetAddr;

//-------------------------
// Initialize listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

//-------------------------
// Bind listening socket
InetAddr.sin_family = AF_INET;
InetAddr.sin_addr.s_addr = htonl(INADDR_ANY);
InetAddr.sin_port = htons(27015);

bind (ListenSocket, (SOCKADDR *) &amp;InetAddr, sizeof(InetAddr));

//-------------------------
// Create new event
NewEvent = WSACreateEvent();

//-------------------------
// Associate event types FD_ACCEPT and FD_CLOSE
// with the listening socket and NewEvent
WSAEventSelect( ListenSocket, NewEvent, FD_ACCEPT | FD_CLOSE);

//----------------------
// Listen for incoming connection requests 
// on the created socket
if (listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR)
    printf("Error listening on socket.\n");

printf("Listening on socket...\n");

// Need an event handler added to handle connection requests


</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a>



<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">shutdown</a>
 

 

