---
UID: NF:winsock2.WSARecvFrom
title: WSARecvFrom function (winsock2.h)
description: Receives a datagram and stores the source address.
helpviewer_keywords: ["WSARecvFrom","WSARecvFrom function [Winsock]","_win32_wsarecvfrom_2","winsock.wsarecvfrom_2","winsock2/WSARecvFrom"]
old-location: winsock\wsarecvfrom_2.htm
tech.root: WinSock
ms.assetid: 8617dbb8-0e4e-4cd3-9597-5d20de6778f6
ms.date: 12/05/2018
ms.keywords: WSARecvFrom, WSARecvFrom function [Winsock], _win32_wsarecvfrom_2, winsock.wsarecvfrom_2, winsock2/WSARecvFrom
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
 - WSARecvFrom
 - winsock2/WSARecvFrom
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
 - WSARecvFrom
---

# WSARecvFrom function


## -description

The 
<b>WSARecvFrom</b> function receives a datagram and stores the source address.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param lpBuffers [in, out]

A pointer to an array of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures. Each 
<b>WSABUF</b> structure contains a pointer to a buffer and the length of the buffer.

### -param dwBufferCount [in]

The number of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures in the <i>lpBuffers</i> array.

### -param lpNumberOfBytesRecvd [out]

A pointer to the number of bytes received by this call if the 
<b>WSARecvFrom</b> operation completes immediately. 

Use <b>NULL</b> for this parameter if the <i>lpOverlapped</i> parameter is not <b>NULL</b> to avoid potentially erroneous results. This parameter can be <b>NULL</b> only if the <i>lpOverlapped</i> parameter is not <b>NULL</b>.

### -param lpFlags [in, out]

A pointer to flags used to modify the behavior of the 
<b>WSARecvFrom</b> function call. See remarks below.

### -param lpFrom [out]

An optional pointer to a buffer that will hold the source address upon the completion of the overlapped operation.

### -param lpFromlen [in, out]

A pointer to the size, in bytes, of the "from" buffer required only if <i>lpFrom</i> is specified.

### -param lpOverlapped [in]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure (ignored for nonoverlapped sockets).

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](./nc-winsock2-lpwsaoverlapped_completion_routine.md)

A pointer to the completion routine called when the 
<b>WSARecvFrom</b> operation has been completed (ignored for nonoverlapped sockets).

## -returns

If no error occurs and the receive operation has completed immediately, 
<b>WSARecvFrom</b> returns zero. In this case, the completion routine will have already been scheduled to be called once the calling thread is in the alertable state. Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>. The error code <b>WSA_IO_PENDING</b> indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that the overlapped operation was not successfully initiated and no completion indication will occur.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was reset by the remote side executing a hard or abortive close. The application should close the socket as it is no longer usable. For a UPD datagram socket, this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffers</i>, <i>lpFlags</i>, <i>lpFrom</i>, <i>lpNumberOfBytesRecvd</i>, <i>lpFromlen</i>, <i>lpOverlapped</i>, or <i>lpCompletionRoutine</i> parameter is not totally contained in a valid part of the user address space: the <i>lpFrom</i> buffer was too small to accommodate the peer address.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound (with 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, for example).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The message was too large for the specified buffer and (for unreliable protocols only) any trailing portion of the message that did not fit into the buffer has been discarded.

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
For a datagram socket, this error indicates that the time to live has expired.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>

Overlapped sockets: There are too many outstanding overlapped I/O requests. Nonoverlapped sockets: The socket is marked as nonblocking and the receive operation cannot be completed immediately.

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
An overlapped operation was successfully initiated and completion will be indicated later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The overlapped operation has been canceled due to the closure of the socket.

</td>
</tr>
</table>

## -remarks

The 
<b>WSARecvFrom</b> function provides functionality over and above the standard 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> function in three important areas:

<ul>
<li>It can be used in conjunction with overlapped sockets to perform overlapped receive operations.</li>
<li>It allows multiple receive buffers to be specified making it applicable to the scatter/gather type of I/O.</li>
<li>The <i>lpFlags</i> parameter is both an input and an output parameter, allowing applications to sense the output state of the <b>MSG_PARTIAL</b> flag bit. Be aware that the <b>MSG_PARTIAL</b> flag bit is not supported by all protocols.</li>
</ul>
The 
<b>WSARecvFrom</b> function is used primarily on a connectionless socket specified by <i>s</i>. The socket's local address must be known. For server applications, this is usually done explicitly through 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>. Explicit binding is discouraged for client applications. For client applications using this function the socket can become bound implicitly to a local address through 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsajoinleaf">WSAJoinLeaf</a>.

For overlapped sockets, this function is used to post one or more buffers into which incoming data will be placed as it becomes available on a (possibly connected) socket, after which the application-specified completion indication (invocation of the completion routine or setting of an event object) occurs. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>. Also, the values indicated by <i>lpFrom</i> and <i>lpFromlen</i> are not updated until completion is itself indicated. Applications must not use or disturb these values until they have been updated; therefore the application must not use automatic (that is, stack-based) variables for these parameters.

<div class="alert"><b>Note</b> All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>
If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>, the socket in this function will be treated as a nonoverlapped socket.

For nonoverlapped sockets, the blocking semantics are identical to that of the standard 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> function and the <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters are ignored. Any data that has already been received and buffered by the transport will be copied into the user buffers. For the case of a blocking socket with no data currently having been received and buffered by the transport, the call will block until data is received.

The buffers are filled in the order in which they appear in the array indicated by <i>lpBuffers</i>, and the buffers are packed so that no holes are created.

If this function is completed in an overlapped manner, it is the Winsock service provider's responsibility to capture the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures before returning from this call. This enables applications to build stack-based 
<b>WSABUF</b> arrays pointed to by the <i>lpBuffers</i> parameter.

For connectionless socket types, the address from which the data originated is copied to the buffer indicated by <i>lpFrom</i>. The value pointed to by <i>lpFromlen</i> is initialized to the size of this buffer, and is modified on completion to indicate the actual size of the address stored there. As stated previously for overlapped sockets, the <i>lpFrom</i> and <i>lpFromlen</i> parameters are not updated until after the overlapped I/O has completed. The memory pointed to by these parameters must, therefore, remain available to the service provider and cannot be allocated on the application stack frame. The <i>lpFrom</i> and <i>lpFromlen</i> parameters are ignored for connection-oriented sockets.

For byte stream–style sockets (for example, type SOCK_STREAM), incoming data is placed into the buffers until:

<ul>
<li>The buffers are filled.</li>
<li>The connection is closed.</li>
<li>The internally buffered data is exhausted.</li>
</ul>
Regardless of whether or not the incoming data fills all the buffers, the completion indication occurs for overlapped sockets. For message-oriented sockets, an incoming message is placed into the buffers up to the total size of the buffers, and the completion indication occurs for overlapped sockets. If the message is larger than the buffers, the buffers are filled with the first part of the message. If the <b>MSG_PARTIAL</b> feature is supported by the underlying service provider, the <b>MSG_PARTIAL</b> flag is set in <i>lpFlags</i> and subsequent receive operation(s) will retrieve the rest of the message. If <b>MSG_PARTIAL</b> is not supported, but the protocol is reliable, 
<b>WSARecvFrom</b> generates the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a> and a subsequent receive operation with a larger buffer can be used to retrieve the entire message. Otherwise, (that is, the protocol is unreliable and does not support <b>MSG_PARTIAL</b>), the excess data is lost, and 
<b>WSARecvFrom</b> generates the error WSAEMSGSIZE.

The <i>lpFlags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>lpFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of any of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>MSG_PEEK</b></td>
<td>Previews the incoming data. The data is copied into the buffer, but is not removed from the input queue. This flag is valid only for nonoverlapped sockets.</td>
</tr>
<tr>
<td><b>MSG_OOB</b></td>
<td>Processes OOB data.</td>
</tr>
<tr>
<td><b>MSG_PARTIAL</b></td>
<td>This flag is for message-oriented sockets only. On output, this flag indicates that the data is a portion of the message transmitted by the sender. Remaining portions of the message will be transmitted in subsequent receive operations. A subsequent receive operation with <b>MSG_PARTIAL</b> flag cleared indicates the end of the sender's message. 


As an input parameter, this flag indicates that the receive operation should complete even if only part of a message has been received by the service provider.

</td>
</tr>
</table>
 

For message-oriented sockets, the <b>MSG_PARTIAL</b> bit is set in the <i>lpFlags</i> parameter if a partial message is received. If a complete message is received, <b>MSG_PARTIAL</b> is cleared in <i>lpFlags</i>. In the case of delayed completion, the value pointed to by <i>lpFlags</i> is not updated. When completion has been indicated the application should call 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> and examine the flags pointed to by the <i>lpdwFlags</i> parameter.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSARecvFrom</b> with the <i>lpOverlapped</i> parameter set to NULL, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Overlapped_Socket_I_O"></a><a id="overlapped_socket_i_o"></a><a id="OVERLAPPED_SOCKET_I_O"></a>Overlapped Socket I/O</h3>
If an overlapped operation completes immediately, 
<b>WSARecvFrom</b> returns a value of zero and the <i>lpNumberOfBytesRecvd</i> parameter is updated with the number of bytes received and the flag bits pointed by the <i>lpFlags</i> parameter are also updated. If the overlapped operation is successfully initiated and will complete later, 
<b>WSARecvFrom</b> returns <b>SOCKET_ERROR</b> and indicates error code <b>WSA_IO_PENDING</b>. In this case, <i>lpNumberOfBytesRecvd</i> and <i>lpFlags</i> is not updated. When the overlapped operation completes the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>. Flag values are obtained either through the <i>dwFlags</i> parameter of the completion routine, or by examining the <i>lpdwFlags</i> parameter of 
<b>WSAGetOverlappedResult</b>.

The 
<b>WSARecvFrom</b> function can be called from within the completion routine of a previous 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<b>WSARecvFrom</b>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> function. For a given socket, I/O completion routines will not be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.

If the <i>lpCompletionRoutine</i> parameter is <b>NULL</b>, the <i>hEvent</i> parameter of <i>lpOverlapped</i> is signaled when the overlapped operation completes if it contains a valid event object handle. An application can use 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not <b>NULL</b>, the <i>hEvent</i> parameter is ignored and can be used by the application to pass context information to the completion routine. A caller that passes a non-<b>NULL</b> <i>lpCompletionRoutine</i> and later calls 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of 
<b>WSAGetOverlappedResult</b> to <b>TRUE</b>. In this case the usage of the <i>hEvent</i> parameter is undefined, and attempting to wait on the <i>hEvent</i> parameter would produce unpredictable results.

The completion routine follows the same rules as stipulated for Windows file I/O completion routines. The completion routine will not be invoked until the thread is in an alertable wait state such as can occur when the function 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> with the <i>fAlertable</i> parameter set to <b>TRUE</b> is invoked.

If an IO completion port is used and the <i>lpCompletionRoutine</i> parameter and the <i>hEvent</i> parameter are <b>NULL</b>, the result of the operation is schedule on the IO completion port. This happens for all successful operations, whether the operations complete immediately or not.

The transport providers allow an application to invoke send and receive operations from within the context of the socket I/O completion routine, and guarantee that, for a given socket, I/O completion routines will not be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The prototype of the completion routine is as follows.


```cpp

void CALLBACK CompletionROUTINE(
  IN DWORD dwError, 
  IN DWORD cbTransferred, 
  IN LPWSAOVERLAPPED lpOverlapped, 
  IN DWORD dwFlags
);

```


The <b>CompletionRoutine</b> is a placeholder for an application-defined or library-defined function name. The <i>dwError</i> specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. The <i>cbTransferred</i> specifies the number of bytes received. The <i>dwFlags</i> parameter contains information that would have appeared in <i>lpFlags</i> if the receive operation had completed immediately. This function does not return a value.

Returning from this function allows invocation of another pending completion routine for this socket. When using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>, all waiting completion routines are called before the alertable thread's wait is satisfied with a return code of WSA_IO_COMPLETION. The completion routines can be called in any order, not necessarily in the same order the overlapped operations are completed. However, the posted buffers are guaranteed to be filled in the same order they are specified.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>WSARecvFrom</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

int __cdecl main()
{

    WSADATA wsaData;
    WSABUF DataBuf;
    WSAOVERLAPPED Overlapped;

    SOCKET RecvSocket = INVALID_SOCKET;
    struct sockaddr_in RecvAddr;
    struct sockaddr_in SenderAddr;

    int SenderAddrSize = sizeof (SenderAddr);
    u_short Port = 27015;

    char RecvBuf[1024];
    int BufLen = 1024;
    DWORD BytesRecv = 0;
    DWORD Flags = 0;

    int err = 0;
    int rc;
    int retval = 0;
    
    //-----------------------------------------------
    // Initialize Winsock
    rc = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (rc != 0) {
        /* Could not find a usable Winsock DLL */
        wprintf(L"WSAStartup failed with error: %ld\n", rc);
        return 1;
    }

    // Make sure the Overlapped struct is zeroed out
    SecureZeroMemory((PVOID) &Overlapped, sizeof(WSAOVERLAPPED) );

    // Create an event handle and setup the overlapped structure.
    Overlapped.hEvent = WSACreateEvent();
    if (Overlapped.hEvent == NULL) {
        wprintf(L"WSACreateEvent failed with error: %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //-----------------------------------------------
    // Create a receiver socket to receive datagrams
    RecvSocket = WSASocket(AF_INET,
                           SOCK_DGRAM,
                           IPPROTO_UDP, NULL, 0, WSA_FLAG_OVERLAPPED);

    if (RecvSocket == INVALID_SOCKET) {
        /* Could not open a socket */
        wprintf(L"WSASocket failed with error: %ld\n", WSAGetLastError());
        WSACloseEvent(Overlapped.hEvent);
        WSACleanup();
        return 1;
    }
    //-----------------------------------------------
    // Bind the socket to any address and the specified port.
    RecvAddr.sin_family = AF_INET;
    RecvAddr.sin_port = htons(Port);
    RecvAddr.sin_addr.s_addr = htonl(INADDR_ANY);

    rc = bind(RecvSocket, (SOCKADDR *) & RecvAddr, sizeof (RecvAddr));
    if (rc != 0) {
        /* Bind to the socket failed */
        wprintf(L"bind failed with error: %ld\n", WSAGetLastError());
        WSACloseEvent(Overlapped.hEvent);
        closesocket(RecvSocket);
        WSACleanup();
        return 1;
    }

    //-----------------------------------------------
    // Call the recvfrom function to receive datagrams
    // on the bound socket.
    DataBuf.len = BufLen;
    DataBuf.buf = RecvBuf;
    wprintf(L"Listening for incoming datagrams on port=%d\n", Port);
    rc = WSARecvFrom(RecvSocket,
                      &DataBuf,
                      1,
                      &BytesRecv,
                      &Flags,
                      (SOCKADDR *) & SenderAddr,
                      &SenderAddrSize, &Overlapped, NULL);

    if (rc != 0) {
        err = WSAGetLastError();
        if (err != WSA_IO_PENDING) {
            wprintf(L"WSARecvFrom failed with error: %ld\n", err);
            WSACloseEvent(Overlapped.hEvent);
            closesocket(RecvSocket);
            WSACleanup();
            return 1;
        }
        else {
            rc = WSAWaitForMultipleEvents(1, &Overlapped.hEvent, TRUE, INFINITE, TRUE);
            if (rc == WSA_WAIT_FAILED) {
                wprintf(L"WSAWaitForMultipleEvents failed with error: %d\n", WSAGetLastError());
                retval = 1;
            }

            rc = WSAGetOverlappedResult(RecvSocket, &Overlapped, &BytesRecv,
                                FALSE, &Flags);
            if (rc == FALSE) {
                wprintf(L"WSArecvFrom failed with error: %d\n", WSAGetLastError());
                retval = 1;
            }
            else
                wprintf(L"Number of received bytes = %d\n", BytesRecv);
                
            wprintf(L"Finished receiving. Closing socket.\n");
        }
        
    }
    //---------------------------------------------
    // When the application is finished receiving, close the socket.

    WSACloseEvent(Overlapped.hEvent);
    closesocket(RecvSocket);
    wprintf(L"Exiting.\n");

    //---------------------------------------------
    // Clean up and quit.
    WSACleanup();
    return (retval);
}

```


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacloseevent">WSACloseEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>