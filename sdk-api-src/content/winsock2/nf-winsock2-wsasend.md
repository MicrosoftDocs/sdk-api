---
UID: NF:winsock2.WSASend
title: WSASend function (winsock2.h)
description: Sends data on a connected socket. (WSASend)
helpviewer_keywords: ["WSASend","WSASend function [Winsock]","_win32_wsasend_2","winsock.wsasend_2","winsock2/WSASend"]
old-location: winsock\wsasend_2.htm
tech.root: WinSock
ms.assetid: 764339e6-a1ac-455d-8ebd-ad0fa50dc3b0
ms.date: 12/05/2018
ms.keywords: WSASend, WSASend function [Winsock], _win32_wsasend_2, winsock.wsasend_2, winsock2/WSASend
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
 - WSASend
 - winsock2/WSASend
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
 - WSASend
---

# WSASend function


## -description

The 
<b>WSASend</b> function sends data on a connected socket.

## -parameters

### -param s [in]

A descriptor that identifies a connected socket.

### -param lpBuffers [in]

A pointer to an array of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures. Each 
<b>WSABUF</b> structure contains a pointer to a buffer and the length, in bytes, of the buffer. For a Winsock application, once the 
<b>WSASend</b> function is called, the system owns these buffers and the application may not access them. This array must remain valid for the duration of the send operation.

### -param dwBufferCount [in]

The number of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures in the <i>lpBuffers</i> array.

### -param lpNumberOfBytesSent [out]

A pointer to the number, in bytes, sent by this call if the I/O operation completes immediately. 

Use <b>NULL</b> for this parameter if the <i>lpOverlapped</i> parameter is not <b>NULL</b> to avoid potentially erroneous results. This parameter can be <b>NULL</b> only  if the <i>lpOverlapped</i> parameter is not <b>NULL</b>.

### -param dwFlags [in]

The flags used to modify the behavior of the 
<b>WSASend</b> function call. For more information, see Using <i>dwFlags</i> in the Remarks section.

### -param lpOverlapped [in]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure. This parameter is ignored for nonoverlapped sockets.

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](./nc-winsock2-lpwsaoverlapped_completion_routine.md)

A pointer to the completion routine called when the send operation has been completed. This parameter is ignored for nonoverlapped sockets.

## -returns

If no error occurs and the send operation has completed immediately, 
<b>WSASend</b> returns zero. In this case, the completion routine will have already been scheduled to be called once the calling thread is in the alertable state. Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>. The error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a> indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that the overlapped operation was not successfully initiated and no completion indication will occur.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was terminated due to a time-out or other failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a stream socket, the virtual circuit was reset by the remote side. The application should close the socket as it is no longer usable. For a UDP datagram socket, this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffers</i>, <i>lpNumberOfBytesSent</i>, <i>lpOverlapped</i>, <i>lpCompletionRoutine</i> parameter is not totally contained in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Socket 1.1 call was canceled through 
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
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> or the socket is not created with the overlapped flag.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a stream socket, the connection has been broken due to keep-alive activity detecting a failure while the operation was in progress. For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
The Windows Sockets provider reports a buffer deadlock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.

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
<b>MSG_OOB</b> was specified, but the socket is not stream-style such as type <b>SOCK_STREAM</b>, OOB data is not supported in the communication domain associated with this socket, <b>MSG_PARTIAL</b> is not supported, or the socket is unidirectional and supports only receive operations.

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
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> on a socket after 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> has been invoked with how set to <b>SD_SEND</b> or <b>SD_BOTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>

Overlapped sockets: There are too many outstanding overlapped I/O requests. Nonoverlapped sockets: The socket is marked as nonblocking and the send operation cannot be completed immediately.

</td>
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The overlapped operation has been canceled due to the closure of the socket, the execution of the "SIO_FLUSH" command in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>, or the thread that initiated the overlapped request exited before the operation completed. For more information, see the Remarks section.

</td>
</tr>
</table>

## -remarks

The 
<b>WSASend</b> function provides functionality over and above the standard 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> function in two important areas:

<ul>
<li>It can be used in conjunction with overlapped sockets to perform overlapped 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> operations.</li>
<li>It allows multiple 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> buffers to be specified making it applicable to the scatter/gather type of I/O.</li>
</ul>
The 
<b>WSASend</b> function is used to write outgoing data from one or more buffers on a connection-oriented socket specified by <i>s</i>. It can also be used, however, on connectionless sockets that have a stipulated default peer address established through the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> function.

A socket created by the <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function will have the overlapped attribute as the default. A socket created by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function with the <i>dwFlags</i> parameter passed to <b>WSASocket</b> with the <b>WSA_FLAG_OVERLAPPED</b> bit set will have the overlapped attribute. For sockets with the overlapped attribute,  <b>WSASend</b> uses overlapped I/O unless both the  <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters are <b>NULL</b>. In that case, the socket is treated as a non-overlapped socket. A completion indication will occur, invoking the completion of a routine or setting of an event object, when the buffer(s) have been consumed by the transport. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>.

If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>, the socket in this function will be treated as a non-overlapped socket.

For non-overlapped sockets, the last two parameters (<i>lpOverlapped</i>, <i>lpCompletionRoutine</i>) are ignored and 
<b>WSASend</b> adopts the same blocking semantics as 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>. Data is copied from the buffer(s) into the transport's buffer. If the socket is non-blocking and stream-oriented, and there is not sufficient space in the transport's buffer, 
<b>WSASend</b> will return with only part of the application's buffers having been consumed. Given the same buffer situation and a blocking socket, 
<b>WSASend</b> will block until all of the application buffer contents have been consumed.

<div class="alert"><b>Note</b>  The socket options <b>SO_RCVTIMEO</b> and <b>SO_SNDTIMEO</b> apply only to blocking sockets.</div>
<div> </div>
If this function is completed in an overlapped manner, it is the Winsock service provider's responsibility to capture the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures before returning from this call. This enables applications to build stack-based 
<b>WSABUF</b> arrays pointed to by the <i>lpBuffers</i> parameter.

For message-oriented sockets, do not exceed the maximum message size of the underlying provider, which can be obtained by getting the value of socket option <b>SO_MAX_MSG_SIZE</b>. If the data is too long to pass atomically through the underlying protocol the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a> is returned, and no data is transmitted.

<b>Windows Me/98/95:  </b>The <b>WSASend</b> function does not support more than 16 buffers.

<div class="alert"><b>Note</b>  The successful completion of a 
<b>WSASend</b> does not indicate that the data was successfully delivered.</div>
<div> </div>
<h3><a id="Using_dwFlags"></a><a id="using_dwflags"></a><a id="USING_DWFLAGS"></a>Using dwFlags</h3>
The <i>dwFlags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>dwFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of any of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>MSG_DONTROUTE</b></td>
<td>Specifies that the data should not be subject to routing. A Windows Sockets service provider can choose to ignore this flag.</td>
</tr>
<tr>
<td><b>MSG_OOB</b></td>
<td>Send OOB data on a stream-style socket such as <b>SOCK_STREAM</b> only.</td>
</tr>
<tr>
<td><b>MSG_PARTIAL</b></td>
<td>Specifies that <i>lpBuffers</i> only contains a partial message. Be aware that the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a> will be returned by transports that do not support partial message transmissions.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSASend</b> with the <i>lpOverlapped</i> parameter set to NULL, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Overlapped_Socket_I_O"></a><a id="overlapped_socket_i_o"></a><a id="OVERLAPPED_SOCKET_I_O"></a>Overlapped Socket I/O</h3>
If an overlapped operation completes immediately, 
<b>WSASend</b> returns a value of zero and the <i>lpNumberOfBytesSent</i> parameter is updated with the number of bytes sent. If the overlapped operation is successfully initiated and will complete later, 
<b>WSASend</b> returns SOCKET_ERROR and indicates error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a>. In this case, <i>lpNumberOfBytesSent</i> is not updated. When the overlapped operation completes the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>.

<div class="alert"><b>Note</b>  All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. For more information, see <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>.</div>
<div> </div>
The 
<b>WSASend</b> function using overlapped I/O can be called from within the completion routine of a previous 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, <b>WSASend</b>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> function. This enables time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.

If the <i>lpCompletionRoutine</i> parameter is <b>NULL</b>, the <i>hEvent</i> parameter of <i>lpOverlapped</i> is signaled when the overlapped operation completes if it contains a valid event object handle. An application can use 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not <b>NULL</b>, the <i>hEvent</i> parameter is ignored and can be used by the application to pass context information to the completion routine. A caller that passes a non-<b>NULL</b> <i>lpCompletionRoutine</i> and later calls 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of 
<b>WSAGetOverlappedResult</b> to <b>TRUE</b>. In this case the usage of the <i>hEvent</i> parameter is undefined, and attempting to wait on the <i>hEvent</i> parameter would produce unpredictable results.

The completion routine follows the same rules as stipulated for Windows file I/O completion routines. The completion routine will not be invoked until the thread is in an alertable wait state such as can occur when the function 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> with the <i>fAlertable</i> parameter set to <b>TRUE</b> is invoked.

The transport providers allow an application to invoke send and receive operations from within the context of the socket I/O completion routine, and guarantee that, for a given socket, I/O completion routines will not be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The following C++ code example is a prototype of the completion routine.


``` syntax

void CALLBACK CompletionROUTINE(
  IN DWORD dwError,
  IN DWORD cbTransferred,
  IN LPWSAOVERLAPPED lpOverlapped,
  IN DWORD dwFlags
);
```

The CompletionRoutine function is a placeholder for an application-defined or library-defined function name. The <i>dwError</i> parameter specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. <i>cbTransferred</i> specifies the number of bytes sent. Currently there are no flag values defined and <i>dwFlags</i> will be zero. This function does not return a value.

Returning from this function allows invocation of another pending completion routine for this socket. All waiting completion routines are called before the alertable thread's wait is satisfied with a return code of <b>WSA_IO_COMPLETION</b>. The completion routines can be called in any order, not necessarily in the same order the overlapped operations are completed. However, the posted buffers are guaranteed to be sent in the same order they are specified.

The order of calls made to <b>WSASend</b> is also the order in which the buffers are transmitted to the transport layer. <b>WSASend</b> should not be called on the same stream-oriented socket concurrently from different threads, because some Winsock providers may split a large send request into multiple transmissions, and this may lead to unintended data interleaving from multiple concurrent send requests on the same stream-oriented socket.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following code example shows how to use the <b>WSASend</b> function in overlapped I/O mode.


```cpp
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h>

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

#define DATA_BUFSIZE 4096
#define SEND_COUNT   10

int __cdecl main()
{
    WSADATA wsd;

    struct addrinfo *result = NULL;
    struct addrinfo hints;
    WSAOVERLAPPED SendOverlapped;

    SOCKET ListenSocket = INVALID_SOCKET;
    SOCKET AcceptSocket = INVALID_SOCKET;

    WSABUF DataBuf;
    DWORD SendBytes;
    DWORD Flags;

    char buffer[DATA_BUFSIZE];

    int err = 0;
    int rc, i;

    // Load Winsock
    rc = WSAStartup(MAKEWORD(2, 2), &wsd);
    if (rc != 0) {
        printf("Unable to load Winsock: %d\n", rc);
        return 1;
    }

    // Make sure the hints struct is zeroed out
    SecureZeroMemory((PVOID) & hints, sizeof(struct addrinfo));

    // Initialize the hints to obtain the 
    // wildcard bind address for IPv4
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    rc = getaddrinfo(NULL, "27015", &hints, &result);
    if (rc != 0) {
        printf("getaddrinfo failed with error: %d\n", rc);
        return 1;
    }

    ListenSocket = socket(result->ai_family,
                          result->ai_socktype, result->ai_protocol);
    if (ListenSocket == INVALID_SOCKET) {
        printf("socket failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        return 1;
    }

    rc = bind(ListenSocket, result->ai_addr, (int) result->ai_addrlen);
    if (rc == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        return 1;
    }

    rc = listen(ListenSocket, 1);
    if (rc == SOCKET_ERROR) {
        printf("listen failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        return 1;
    }
    // Accept an incoming connection request
    AcceptSocket = accept(ListenSocket, NULL, NULL);
    if (AcceptSocket == INVALID_SOCKET) {
        printf("accept failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        return 1;
    }

    printf("Client Accepted...\n");

    // Make sure the SendOverlapped struct is zeroed out
    SecureZeroMemory((PVOID) & SendOverlapped, sizeof (WSAOVERLAPPED));

    // Create an event handle and setup the overlapped structure.
    SendOverlapped.hEvent = WSACreateEvent();
    if (SendOverlapped.hEvent == NULL) {
        printf("WSACreateEvent failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        closesocket(AcceptSocket);
        return 1;
    }

    DataBuf.len = DATA_BUFSIZE;
    DataBuf.buf = buffer;

    for (i = 0; i < SEND_COUNT; i++) {

        rc = WSASend(AcceptSocket, &DataBuf, 1,
                     &SendBytes, 0, &SendOverlapped, NULL);
        if ((rc == SOCKET_ERROR) &&
            (WSA_IO_PENDING != (err = WSAGetLastError()))) {
            printf("WSASend failed with error: %d\n", err);
            break;
        }

        rc = WSAWaitForMultipleEvents(1, &SendOverlapped.hEvent, TRUE, INFINITE,
                                      TRUE);
        if (rc == WSA_WAIT_FAILED) {
            printf("WSAWaitForMultipleEvents failed with error: %d\n",
                   WSAGetLastError());
            break;
        }

        rc = WSAGetOverlappedResult(AcceptSocket, &SendOverlapped, &SendBytes,
                                    FALSE, &Flags);
        if (rc == FALSE) {
            printf("WSASend failed with error: %d\n", WSAGetLastError());
            break;
        }

        printf("Wrote %d bytes\n", SendBytes);

        WSAResetEvent(SendOverlapped.hEvent);

    }

    WSACloseEvent(SendOverlapped.hEvent);
    closesocket(AcceptSocket);
    closesocket(ListenSocket);
    freeaddrinfo(result);

    WSACleanup();

    return 0;
}


```


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
