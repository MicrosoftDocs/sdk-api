---
UID: NF:winsock2.WSAGetOverlappedResult
title: WSAGetOverlappedResult function
author: windows-sdk-content
description: The WSAGetOverlappedResult function retrieves the results of an overlapped operation on the specified socket.
old-location: winsock\wsagetoverlappedresult_2.htm
tech.root: winsock
ms.assetid: 3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSAGetOverlappedResult, WSAGetOverlappedResult function [Winsock], _win32_wsagetoverlappedresult_2, winsock.wsagetoverlappedresult_2, winsock2/WSAGetOverlappedResult
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSAGetOverlappedResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAGetOverlappedResult function


## -description


The 
<b>WSAGetOverlappedResult</b> function retrieves the results of an overlapped operation on the specified socket.


## -parameters




### -param s [in]

A descriptor identifying the socket. 

This is the same socket that was specified when the overlapped operation was started by a call to 
any of the Winsock functions that supports overlappped operations. These functions include <a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>, <a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>, <a href="https://msdn.microsoft.com/220ba610-1694-470d-8b5e-e6b5fc3b4d0b">DisconnectEx</a>, <a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>, <a href="https://msdn.microsoft.com/c574d320-2a90-40bb-b34c-6023e80514e6">TransmitPackets</a>, <a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>, 
<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>, 
<a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>, <a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>, 
<a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a>, <a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>, and 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>.


### -param lpOverlapped [in]

A pointer to a 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure that was specified when the overlapped operation was started. This parameter must not be a <b>NULL</b> pointer.


### -param lpcbTransfer [out]

A pointer to a 32-bit variable that receives the number of bytes that were actually transferred by a send or receive operation, or by 
the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function. This parameter must not be a <b>NULL</b> pointer.


### -param fWait [in]

A flag that specifies whether the function should wait for the pending overlapped operation to complete. If <b>TRUE</b>, the function does not return until the operation has been completed. If <b>FALSE</b> and the operation is still pending, the function returns <b>FALSE</b> and the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function returns WSA_IO_INCOMPLETE. The <i>fWait</i> parameter may be set to <b>TRUE</b> only if the overlapped operation selected the event-based completion notification.


### -param lpdwFlags [out]

A pointer to a 32-bit variable that will receive one or more flags that supplement the completion status. If the overlapped operation was initiated through 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> or 
<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>, this parameter will contain the results value for <i>lpFlags</i> parameter. This parameter must not be a <b>NULL</b> pointer.


## -returns



If 
<b>WSAGetOverlappedResult</b> succeeds, the return value is <b>TRUE</b>. This means that the overlapped operation has completed successfully and that the value pointed to by <i>lpcbTransfer</i> has been updated. 

If 
<b>WSAGetOverlappedResult</b> returns <b>FALSE</b>, this means that either the overlapped operation has not completed, the overlapped operation completed but with errors, or the overlapped operation's completion status could not be determined due to errors in one or more parameters to 
<b>WSAGetOverlappedResult</b>. On failure, the value pointed to by <i>lpcbTransfer</i> will not be updated. Use 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> to determine the cause of the failure (either by the <b>WSAGetOverlappedResult</b> function or by the associated overlapped operation).

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter of the 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure does not contain a valid event object handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_PARAMETER</a></b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is unacceptable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_IO_INCOMPLETE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>fWait</i> parameter is <b>FALSE</b> and the I/O operation has not yet completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
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
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure that was specified when the overlapped function was called. A pending operation is indicated when the function that started the operation returns <b>FALSE</b> and the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function returns <a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a>. When an I/O operation such as 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> is pending, the function that started the operation resets the <i>hEvent</i> member of the 
<b>WSAOVERLAPPED</b> structure to the nonsignaled state. Then, when the pending operation has completed, the system sets the event object to the signaled state.

If the <i>fWait</i> parameter is <b>TRUE</b>, 
<b>WSAGetOverlappedResult</b> determines whether the pending operation has been completed by waiting for the event object to be in the signaled state. A client may set the <i>fWait</i> parameter to <b>TRUE</b>, but only if it selected event-based completion notification when the I/O operation was requested. If another form of notification was selected, the usage of the <i>hEvent</i> parameter of the 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure is different, and setting <i>fWait</i> to <b>TRUE</b> causes unpredictable results.

If the <b>WSAGetOverlappedResult</b> function is called with the <i>lpOverlapped</i>, <i>lpcbTransfer</i>, or <i>lpdwFlags</i> parameter  set to a <b>NULL</b> pointer on Windows Vista, this will result in an access violation. If the <b>WSAGetOverlappedResult</b> function is called with the <i>lpOverlapped</i>, <i>lpcbTransfer</i>, or <i>lpdwFlags</i> parameter  set to a <b>NULL</b> pointer on Windows Server 2003 and earlier, this will result in the <a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a> error code being returned.  

<div class="alert"><b>Note</b>   All I/O is canceled when a thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>



<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>



<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>



<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>



<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

