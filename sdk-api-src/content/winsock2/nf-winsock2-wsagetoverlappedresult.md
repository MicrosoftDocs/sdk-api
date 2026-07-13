---
UID: NF:winsock2.WSAGetOverlappedResult
title: WSAGetOverlappedResult function (winsock2.h)
description: The WSAGetOverlappedResult function retrieves the results of an overlapped operation on the specified socket.
helpviewer_keywords: ["WSAGetOverlappedResult","WSAGetOverlappedResult function [Winsock]","_win32_wsagetoverlappedresult_2","winsock.wsagetoverlappedresult_2","winsock2/WSAGetOverlappedResult"]
old-location: winsock\wsagetoverlappedresult_2.htm
tech.root: WinSock
ms.assetid: 3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4
ms.date: 12/05/2018
ms.keywords: WSAGetOverlappedResult, WSAGetOverlappedResult function [Winsock], _win32_wsagetoverlappedresult_2, winsock.wsagetoverlappedresult_2, winsock2/WSAGetOverlappedResult
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
 - WSAGetOverlappedResult
 - winsock2/WSAGetOverlappedResult
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
 - WSAGetOverlappedResult
---

# WSAGetOverlappedResult function


## -description

The 
<b>WSAGetOverlappedResult</b> function retrieves the results of an overlapped operation on the specified socket.

## -parameters

### -param s [in]

A descriptor identifying the socket. 

This is the same socket that was specified when the overlapped operation was started by a call to 
any of the Winsock functions that supports overlapped operations. These functions include <a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>, <a href="/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)">DisconnectEx</a>, <a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_transmitpackets">TransmitPackets</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, 
<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>.

### -param lpOverlapped [in]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure that was specified when the overlapped operation was started. This parameter must not be a <b>NULL</b> pointer.

### -param lpcbTransfer [out]

A pointer to a 32-bit variable that receives the number of bytes that were actually transferred by a send or receive operation, or by 
the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function. This parameter must not be a <b>NULL</b> pointer.

### -param fWait [in]

A flag that specifies whether the function should wait for the pending overlapped operation to complete. If <b>TRUE</b>, the function does not return until the operation has been completed. If <b>FALSE</b> and the operation is still pending, the function returns <b>FALSE</b> and the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function returns WSA_IO_INCOMPLETE. The <i>fWait</i> parameter may be set to <b>TRUE</b> only if the overlapped operation selected the event-based completion notification.

### -param lpdwFlags [out]

A pointer to a 32-bit variable that will receive one or more flags that supplement the completion status. If the overlapped operation was initiated through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, this parameter will contain the results value for <i>lpFlags</i> parameter. This parameter must not be a <b>NULL</b> pointer.

## -returns

If 
<b>WSAGetOverlappedResult</b> succeeds, the return value is <b>TRUE</b>. This means that the overlapped operation has completed successfully and that the value pointed to by <i>lpcbTransfer</i> has been updated. 

If 
<b>WSAGetOverlappedResult</b> returns <b>FALSE</b>, this means that either the overlapped operation has not completed, the overlapped operation completed but with errors, or the overlapped operation's completion status could not be determined due to errors in one or more parameters to 
<b>WSAGetOverlappedResult</b>. On failure, the value pointed to by <i>lpcbTransfer</i> will not be updated. Use 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> to determine the cause of the failure (either by the <b>WSAGetOverlappedResult</b> function or by the associated overlapped operation).

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter of the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure does not contain a valid event object handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is unacceptable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_INCOMPLETE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>fWait</i> parameter is <b>FALSE</b> and the I/O operation has not yet completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the <i>lpOverlapped</i>, <i>lpcbTransfer</i>, or <i>lpdwFlags</i> parameters are not in a valid part of the user address space. This error is returned if the <i>lpOverlapped</i>, <i>lpcbTransfer</i>, or <i>lpdwFlags</i> parameter  was a <b>NULL</b> pointer on Windows Server 2003 and earlier.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAGetOverlappedResult</b> function reports the results of the overlapped operation specified in the <i>lpOverlapped</i> parameter for the socket specified in the <i>s</i> parameter. The 
<b>WSAGetOverlappedResult</b> function is passed the socket descriptor and the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure that was specified when the overlapped function was called. A pending operation is indicated when the function that started the operation returns <b>FALSE</b> and the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a>. When an I/O operation such as 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> is pending, the function that started the operation resets the <i>hEvent</i> member of the 
<b>WSAOVERLAPPED</b> structure to the nonsignaled state. Then, when the pending operation has completed, the system sets the event object to the signaled state.

If the <i>fWait</i> parameter is <b>TRUE</b>, 
<b>WSAGetOverlappedResult</b> determines whether the pending operation has been completed by waiting for the event object to be in the signaled state. A client may set the <i>fWait</i> parameter to <b>TRUE</b>, but only if it selected event-based completion notification when the I/O operation was requested. If another form of notification was selected, the usage of the <i>hEvent</i> parameter of the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure is different, and setting <i>fWait</i> to <b>TRUE</b> causes unpredictable results.

If the <b>WSAGetOverlappedResult</b> function is called with the <i>lpOverlapped</i>, <i>lpcbTransfer</i>, or <i>lpdwFlags</i> parameter  set to a <b>NULL</b> pointer on Windows Vista, this will result in an access violation. If the <b>WSAGetOverlappedResult</b> function is called with the <i>lpOverlapped</i>, <i>lpcbTransfer</i>, or <i>lpdwFlags</i> parameter  set to a <b>NULL</b> pointer on Windows Server 2003 and earlier, this will result in the <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a> error code being returned.  

<div class="alert"><b>Note</b>   All I/O is canceled when a thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>