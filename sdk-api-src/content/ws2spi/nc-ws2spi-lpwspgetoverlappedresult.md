---
UID: NC:ws2spi.LPWSPGETOVERLAPPEDRESULT
title: LPWSPGETOVERLAPPEDRESULT
description: The LPWSPGetOverlappedResult function returns the results of an overlapped operation on the specified socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPGETOVERLAPPEDRESULT"]
ms.date: 4/26/2019
ms.keywords: LPWSPGETOVERLAPPEDRESULT
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - ws2spi.h
api_name:
 - LPWSPGETOVERLAPPEDRESULT
f1_keywords:
 - LPWSPGETOVERLAPPEDRESULT
 - ws2spi/LPWSPGETOVERLAPPEDRESULT
---

## -description

The **LPWSPGetOverlappedResult** function returns the results of an overlapped operation on the specified socket.

## -parameters

### -param s [in]

Identifies the socket. This is the same socket that was specified when the overlapped operation was started by a call to <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b>, or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>.

### -param lpOverlapped [in]

Pointer to a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure that was specified when the overlapped operation was started.

### -param lpcbTransfer [out]

Pointer to a 32-bit variable that receives the number of bytes that were actually transferred by a send or receive operation, or by <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>.

### -param fWait [in]

Specifies whether the function should wait for the pending overlapped operation to complete. If **TRUE**, the function does not return until the operation has been completed. If **FALSE** and the operation is still pending, the function returns **FALSE** and <i>lpErrno</i> is WSA_IO_INCOMPLETE. The <i>fWait</i> parameter may be set to **TRUE** only if the overlapped operation selected event-based completion notification.

### -param lpdwFlags [out]

Pointer to a 32-bit variable that will receive one or more flags that supplement the completion status. If the overlapped operation was initiated through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b> or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b>, this parameter will contain the results value for <i>lpFlags</i> parameter.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If **LPWSPGetOverlappedResult** succeeds, the return value is **TRUE**. This means the overlapped operation has completed successfully and the value pointed to by <i>lpcbTransfer</i> has been updated. If **LPWSPGetOverlappedResult** returns **FALSE**, this means that the overlapped operation has not completed or the overlapped operation completed but with errors, or completion status could not be determined due to errors in one or more parameters to **LPWSPGetOverlappedResult**. On failure, the value pointed to by <i>lpcbTransfer</i> will not be updated. The <i>lpErrno</i> parameter indicates the cause of the failure (either of **LPWSPGetOverlappedResult** or of the associated overlapped operation).

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSA_INVALID_HANDLE">WSA_INVALID_HANDLE</a></dt>
</dl>
</td>
<td width="60%">
The **hEvent** member of the <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure does not contain a valid event object handle.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
One of the parameters is unacceptable.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSA_IO_INCOMPLETE">WSA_IO_INCOMPLETE</a></dt>
</dl>
</td>
<td width="60%">
The <i>fWait</i> parameter is **FALSE** and the I/O operation has not yet completed.  
</td>
</tr>
</table>

## -remarks

The results reported by the **LPWSPGetOverlappedResult** function are those of the specified socket's last overlapped operation to which the specified <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure was provided, and for which the operation's results were pending. A pending operation is indicated when the function that started the operation returns SOCKET_ERROR, and the <i>lpErrno</i> is WSA_IO_PENDING. When an I/O operation is pending, the function that started the operation resets the **hEvent** member of the **WSAOVERLAPPED** structure to the nonsignaled state. Then, when the pending operation has been completed, the system sets the event object to the signaled state.

If the <i>fWait</i> parameter is **TRUE**, **LPWSPGetOverlappedResult** determines whether the pending operation has been completed by blocking and waiting for the event object to be in the signaled state. A client may set the <i>fWait</i> parameter to **TRUE** only if it selected event-based completion notification when the I/O operation was requested. If another form of notification was selected, the usage of the **hEvent** member of the <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure is different, and setting <i>fWait</i> to **TRUE** causes unpredictable results.

> [!Note]  
> All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the operations complete. See <b><a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a></b> for more information.

 

### Interaction with WPUCompleteOverlappedRequest

The behavior of <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucompleteoverlappedrequest">WPUCompleteOverlappedRequest</a></b> places some constraints on how a service provider implements **LPWSPGetOverlappedResult** since only the **Offset** and **OffsetHigh** members of the <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure are exclusively controlled by the service provider even though three values (byte count, flags, and error) must be retrieved from the structure by **LPWSPGetOverlappedResult**. A service provider may accomplish this any way it chooses as long as it interacts with the behavior of **WPUCompleteOverlappedRequest** properly. The following description presents a typical implementation:

At the start of overlapped processing, the service provider sets **Internal** to WSS_OPERATION_IN_PROGRESS.

When the I/O operation is complete, the provider sets **OffsetHigh** to the Windows Sockets 2 error code resulting from the operation, sets **Offset** to the flags resulting from the I/O operation, and calls <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucompleteoverlappedrequest">WPUCompleteOverlappedRequest</a></b>, passing the transfer byte count as one of the parameters. **WPUCompleteOverlappedRequest** eventually sets **InternalHigh** to the transfer byte count, then sets **Internal** to a value other than WSS_OPERATION_IN_PROGRESS.

When **LPWSPGetOverlappedResult** is called, the service provider checks Internal. If it is WSS_OPERATION_IN_PROGRESS, the provider waits on the event handle in the **hEvent** member or returns an error, based on the setting of the <i>fWait</i> flag of **LPWSPGetOverlappedResult**. If not in progress, or after completion of waiting, the provider returns the values from **InternalHigh**, **OffsetHigh**, and **Offset** as the transfer count, operation result error code, and flags respectively.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucompleteoverlappedrequest">WPUCompleteOverlappedRequest</a>

[LPWSPAccept](nc-ws2spi-lpwspaccept.md)

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a>

