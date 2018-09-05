---
UID: NF:winsock2.WSASendTo
title: WSASendTo function
author: windows-sdk-content
description: Sends data to a specific destination, using overlapped I/O where applicable.
old-location: winsock\wsasendto_2.htm
old-project: WinSock
ms.assetid: e3a11522-871c-4d6b-a2e6-ca91ffc2b698
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSASendTo, WSASendTo function [Winsock], _win32_wsasendto_2, winsock.wsasendto_2, winsock2/WSASendTo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.redist: 
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
 - WSASendTo
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSASendTo function


## -description


The 
<b>WSASendTo</b> function sends data to a specific destination, using overlapped I/O where applicable.


## -parameters




### -param s [in]

A descriptor identifying a (possibly connected) socket.


### -param lpBuffers [in]

A pointer to an array of 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structures. Each 
<b>WSABUF</b> structure contains a pointer to a buffer and the length of the buffer, in bytes. For a Winsock application, once the 
<b>WSASendTo</b> function is called, the system owns these buffers and the application may not access them. This array must remain valid for the duration of the send operation.


### -param dwBufferCount [in]

The number of 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structures in the <i>lpBuffers</i> array.


### -param lpNumberOfBytesSent [out]

A pointer to the number of bytes sent by this call if the I/O operation completes immediately. 

Use <b>NULL</b> for this parameter if the <i>lpOverlapped</i> parameter is not <b>NULL</b> to avoid potentially erroneous results. This parameter can be <b>NULL</b> only  if the <i>lpOverlapped</i> parameter is not <b>NULL</b>.


### -param dwFlags [in]

The flags  used to modify the behavior of the 
<b>WSASendTo</b> function call.


### -param lpTo [in]

An optional pointer to the address of the target socket in the 
<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR</a> structure.


### -param iTolen [in]

The size, in bytes, of the address in the <i>lpTo</i> parameter.


### -param lpOverlapped [in]

A pointer to a 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure (ignored for nonoverlapped sockets).


### -param lpCompletionRoutine [in]

A pointer to the completion routine called when the send operation has been completed (ignored for nonoverlapped sockets).


## -returns



If no error occurs and the send operation has completed immediately, 
<b>WSASendTo</b> returns zero. In this case, the completion routine will have already been scheduled to be called once the calling thread is in the alertable state. Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>. The error code <a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a> indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that the overlapped operation was not successfully initiated and no completion indication will occur.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The requested address is a broadcast address, but the appropriate flag was not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address (such as ADDR_ANY).

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a UDP datagram socket, this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEDESTADDRREQ</a></b></dt>
</dl>
</td>
<td width="60%">
A destination address is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffers</i>, <i>lpTo</i>, <i>lpOverlapped</i>, <i>lpNumberOfBytesSent</i>, or <i>lpCompletionRoutine</i> parameters are not part of the user address space, or the <i>lpTo</i> parameter is too small.

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Socket 1.1 call was canceled through 
<a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound with 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, or the socket is not created with the overlapped flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is message oriented, and the message is larger than the maximum supported by the underlying transport.

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a datagram socket, this error indicates that the time to live has expired.

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
The Windows Sockets provider reports a buffer deadlock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected (connection-oriented sockets only).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to 
<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a> on a socket after 
<a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> has been invoked with <i>how</i> set to SD_SEND or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>

Overlapped sockets: there are too many outstanding overlapped I/O requests. Nonoverlapped sockets: The socket is marked as nonblocking and the send operation cannot be completed immediately.

</td>
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The overlapped operation has been canceled due to the closure of the socket, or the execution of the SIO_FLUSH command in 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSASendTo</b> function provides enhanced features over the standard 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> function in two important areas:

<ul>
<li>It can be used in conjunction with overlapped sockets to perform overlapped send operations.</li>
<li>It allows multiple send buffers to be specified making it applicable to the scatter/gather type of I/O.</li>
</ul>
The 
<b>WSASendTo</b> function is normally used on a connectionless socket specified by <i>s</i> to send a datagram contained in one or more buffers to a specific peer socket identified by the <i>lpTo</i> parameter. Even if the connectionless socket has been previously connected using the 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> function to a specific address, <i>lpTo</i> overrides the destination address for that particular datagram only. On a connection-oriented socket, the <i>lpTo</i> and <i>iToLen</i> parameters are ignored; in this case, the 
<b>WSASendTo</b> is equivalent to 
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>.

For overlapped sockets (created using 
<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> with flag <b>WSA_FLAG_OVERLAPPED</b>) sending data uses overlapped I/O, unless both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b> in which case the socket is treated as a nonoverlapped socket. A completion indication will occur (invoking the completion routine or setting of an event object) when the buffer(s) have been consumed by the transport. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>.

<div class="alert"><b>Note</b>  If a socket is opened, a 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> call is made, and then a 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function call.</div>
<div> </div>
If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>, the socket in this function will be treated as a nonoverlapped socket.

For nonoverlapped sockets, the last two parameters (<i>lpOverlapped</i>, <i>lpCompletionRoutine</i>) are ignored and 
<b>WSASendTo</b> adopts the same blocking semantics as 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>. Data is copied from the buffer(s) into the transport buffer. If the socket is nonblocking and stream oriented, and there is not sufficient space in the transport's buffer, 
<b>WSASendTo</b> returns with only part of the application's buffers having been consumed. Given the same buffer situation and a blocking socket, 
<b>WSASendTo</b> will block until all of the application's buffer contents have been consumed.

If this function is completed in an overlapped manner, it is the Winsock service provider's responsibility to capture the 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structures before returning from this call. This enables applications to build stack-based 
<b>WSABUF</b> arrays pointed to by the <i>lpBuffers</i> parameter.

For message-oriented sockets, care must be taken not to exceed the maximum message size of the underlying transport, which can be obtained by getting the value of socket option <b>SO_MAX_MSG_SIZE</b>. If the data is too long to pass atomically through the underlying protocol the error 
<a href="windows_sockets_error_codes_2.htm">WSAEMSGSIZE</a> is returned, and no data is transmitted.

If the socket is unbound, unique values are assigned to the local association by the system, and the socket is then marked as bound. 

If the socket is connected, the <a href="https://msdn.microsoft.com/be20a731-cdfc-48ae-90b2-43f2cf9ecf6d">getsockname</a> function can be used to determine the local IP address and port associated with the socket. 

If the socket is not connected, the  
<a href="https://msdn.microsoft.com/be20a731-cdfc-48ae-90b2-43f2cf9ecf6d">getsockname</a>   function can be used to determine the local port number associated with the socket but the IP address returned is set to the wildcard address for the given protocol (for example, INADDR_ANY  or "0.0.0.0" for IPv4 and IN6ADDR_ANY_INIT or "::" for IPv6).

The successful completion of a 
<b>WSASendTo</b> does not indicate that the data was successfully delivered.

The <i>dwFlags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>dwFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of any of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>MSG_DONTROUTE</b></td>
<td>Specifies that the data should not be subject to routing. A Windows Socket service provider may choose to ignore this flag.</td>
</tr>
<tr>
<td><b>MSG_OOB</b></td>
<td>Send OOB data (stream-style socket such as <b>SOCK_STREAM</b> only).</td>
</tr>
<tr>
<td><b>MSG_PARTIAL</b></td>
<td>Specifies that <i>lpBuffers</i> only contains a partial message. Be aware that the error code 
<a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a> will be returned by transports that do not support partial message transmissions.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSASendTo</b> with the <i>lpOverlapped</i> parameter set to <b>NULL</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Overlapped_Socket_I_O"></a><a id="overlapped_socket_i_o"></a><a id="OVERLAPPED_SOCKET_I_O"></a>Overlapped Socket I/O</h3>
If an overlapped operation completes immediately, 
<b>WSASendTo</b> returns a value of zero and the <i>lpNumberOfBytesSent</i> parameter is updated with the number of bytes sent. If the overlapped operation is successfully initiated and will complete later, 
<b>WSASendTo</b> returns <b>SOCKET_ERROR</b> and indicates error code 
<a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a>. In this case, <i>lpNumberOfBytesSent</i> is not updated. When the overlapped operation completes the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>
The 
<b>WSASendTo</b> function using overlapped I/O can be called from within the completion routine of a previous 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>, 
<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>, 
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>, or 
<b>WSASendTo</b> function. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure.

If the <i>lpCompletionRoutine</i> parameter is <b>NULL</b>, the <i>hEvent</i> parameter of <i>lpOverlapped</i> is signaled when the overlapped operation completes if it contains a valid event object handle. An application can use 
<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a> or 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not <b>NULL</b>, the <i>hEvent</i> parameter is ignored and can be used by the application to pass context information to the completion routine. A caller that passes a non-<b>NULL</b><i>lpCompletionRoutine</i> and later calls 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of 
<b>WSAGetOverlappedResult</b> to <b>TRUE</b>. In this case the usage of the <i>hEvent</i> parameter is undefined, and attempting to wait on the <i>hEvent</i> parameter would produce unpredictable results.

The completion routine follows the same rules as stipulated for Windows file I/O completion routines. The completion routine will not be invoked until the thread is in an alertable wait state such as can occur when the function 
<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a> with the <i>fAlertable</i> parameter set to <b>TRUE</b> is invoked.

Transport providers allow an application to invoke send and receive operations from within the context of the socket I/O completion routine, and guarantee that, for a given socket, I/O completion routines will not be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The prototype of the completion routine is as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
void CALLBACK CompletionROUTINE(
  IN DWORD dwError,
  IN DWORD cbTransferred,
  IN LPWSAOVERLAPPED lpOverlapped,
  IN DWORD dwFlags
);
</pre>
</td>
</tr>
</table></span></div>
The  CompletionRoutine function is a placeholder for an application-defined or library-defined function name. The <i>dwError</i> parameter specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. The <i>cbTransferred</i> parameter specifies the number of bytes sent. Currently there are no flag values defined and <i>dwFlags</i> will be zero. This function does not return a value.

Returning from this function allows invocation of another pending completion routine for this socket. All waiting completion routines are called before the alertable thread's wait is satisfied with a return code of WSA_IO_COMPLETION. The completion routines can be called in any order, not necessarily in the same order in which the overlapped operations are completed. However, the posted buffers are guaranteed to be sent in the same order they are specified.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>WSASendTo</b> function using an event object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define WIN32_LEAN_AND_MEAN

#include &lt;winsock2.h&gt;
#include &lt;Ws2tcpip.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    //---------------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    WSABUF DataBuf;

    WSAOVERLAPPED Overlapped;
    SOCKET SendToSocket = INVALID_SOCKET;

    struct sockaddr_in RecvAddr;
    struct sockaddr_in LocalAddr;
    int RecvAddrSize = sizeof (RecvAddr);
    int LocalAddrSize = sizeof (LocalAddr);

    u_short Port = 27777;
    struct hostent *localHost;
    char *ip;
    
    char *targetip;
    char *targetport;

    char SendBuf[1024] = "Data buffer to send";
    int BufLen = 1024;
    DWORD BytesSent = 0;
    DWORD Flags = 0;

    int rc, err;
    int retval = 0;

    // Validate the parameters
    if (argc != 3) {
        printf("usage: %s targetip port\n", argv[0]);
        printf("  to sendto the localhost on port 27777\n");
        printf("       %s 127.0.0.1 27777\n", argv[0]);
        return 1;
    }

    targetip = argv[1];
    targetport = argv[2];

    //---------------------------------------------
    // Initialize Winsock
    // Load Winsock
    rc = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
    if (rc != 0) {
        printf("Unable to load Winsock: %d\n", rc);
        return 1;
    }

    // Make sure the Overlapped struct is zeroed out
    SecureZeroMemory((PVOID) &amp;Overlapped, sizeof(WSAOVERLAPPED));

    // Create an event handle and setup the overlapped structure.
    Overlapped.hEvent = WSACreateEvent();
    if (Overlapped.hEvent == WSA_INVALID_EVENT) {
        printf("WSACreateEvent failed with error: %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //---------------------------------------------
    // Create a socket for sending data
    SendToSocket =
        WSASocket(AF_INET, SOCK_DGRAM, IPPROTO_UDP, NULL, 0,
                  WSA_FLAG_OVERLAPPED);
    if (SendToSocket == INVALID_SOCKET) {
        printf("socket failed with error: %d\n", WSAGetLastError());
        WSACloseEvent(Overlapped.hEvent);
        WSACleanup();
        return 1;
    }
    //---------------------------------------------
    // Set up the RecvAddr structure with the IP address of
    // the receiver (in this example case "123.123.123.1")
    // and the specified port number.
    RecvAddr.sin_family = AF_INET;

    RecvAddr.sin_addr.s_addr = inet_addr(targetip);
    if (RecvAddr.sin_addr.s_addr == INADDR_NONE)  {
        printf("The target ip address entered must be a legal IPv4 address\n");
        WSACloseEvent(Overlapped.hEvent);
        WSACleanup();
        return 1;
    }
    RecvAddr.sin_port = htons( (u_short) atoi(targetport));
    if(RecvAddr.sin_port == 0) {
        printf("The targetport must be a legal UDP port number\n");
        WSACloseEvent(Overlapped.hEvent);
        WSACleanup();
        return 1;
    }

    //---------------------------------------------
    // Set up the LocalAddr structure with the local IP address
    // and the specified port number.
    localHost = gethostbyname("");
    ip = inet_ntoa(*(struct in_addr *) *localHost-&gt;h_addr_list);

    LocalAddr.sin_family = AF_INET;
    LocalAddr.sin_addr.s_addr = inet_addr(ip);
    LocalAddr.sin_port = htons(Port);

    //---------------------------------------------
    // Bind the sending socket to the LocalAddr structure
    // that has the internet address family, local IP address
    // and specified port number.  
    rc = bind(SendToSocket, (struct sockaddr *) &amp;LocalAddr, LocalAddrSize);
    if (rc == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        WSACloseEvent(Overlapped.hEvent);
        closesocket(SendToSocket);
        WSACleanup();
        return 1;
    }
    //---------------------------------------------
    // Send a datagram to the receiver
    printf("Sending datagram from IPv4 address = %s port=%d\n", 
       inet_ntoa(LocalAddr.sin_addr), ntohs(LocalAddr.sin_port) ); 
    printf("   to IPv4 address = %s port=%d\n", 
       inet_ntoa(RecvAddr.sin_addr), ntohs(RecvAddr.sin_port) ); 

//    printf("Sending a datagram...\n");
    DataBuf.len = BufLen;
    DataBuf.buf = SendBuf;
    rc = WSASendTo(SendToSocket, &amp;DataBuf, 1,
                   &amp;BytesSent, Flags, (SOCKADDR *) &amp; RecvAddr,
                   RecvAddrSize, &amp;Overlapped, NULL);

    if ((rc == SOCKET_ERROR) &amp;&amp; (WSA_IO_PENDING != (err = WSAGetLastError()))) {
        printf("WSASendTo failed with error: %d\n", err);
        WSACloseEvent(Overlapped.hEvent);
        closesocket(SendToSocket);
        WSACleanup();
        return 1;
    }

    rc = WSAWaitForMultipleEvents(1, &amp;Overlapped.hEvent, TRUE, INFINITE, TRUE);
    if (rc == WSA_WAIT_FAILED) {
        printf("WSAWaitForMultipleEvents failed with error: %d\n",
                WSAGetLastError());
        retval = 1;
    }

    rc = WSAGetOverlappedResult(SendToSocket, &amp;Overlapped, &amp;BytesSent,
                                FALSE, &amp;Flags);
    if (rc == FALSE) {
        printf("WSASendTo failed with error: %d\n", WSAGetLastError());
        retval = 1;
    }
    else
        printf("Number of sent bytes = %d\n", BytesSent);
        
    //---------------------------------------------
    // When the application is finished sending, close the socket.
    printf("Finished sending. Closing socket.\n");
    WSACloseEvent(Overlapped.hEvent);
    closesocket(SendToSocket);
    printf("Exiting.\n");

    //---------------------------------------------
    // Clean up and quit.
    WSACleanup();
    return (retval);
}
</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>



<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

