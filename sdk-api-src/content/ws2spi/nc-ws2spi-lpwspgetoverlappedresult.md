---
UID: NC:ws2spi.LPWSPGETOVERLAPPEDRESULT
title: LPWSPGETOVERLAPPEDRESULT
author: windows-sdk-content
description: The WSPGetOverlappedResult function returns the results of an overlapped operation on the specified socket.
old-location: winsock\wspgetoverlappedresult_2.htm
tech.root: winsock
ms.assetid: 8156b8ab-00f8-4325-9b81-3e43053f4f56
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LPWSPGETOVERLAPPEDRESULT, WSPGetOverlappedResult, WSPGetOverlappedResult function [Winsock], _win32_wspgetoverlappedresult_2, winsock.wspgetoverlappedresult_2, ws2spi/WSPGetOverlappedResult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WSPGetOverlappedResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPWSPGETOVERLAPPEDRESULT callback function


## -description


The 
<b>WSPGetOverlappedResult</b> function returns the results of an overlapped operation on the specified socket.


## -parameters




### -param s [in]

Identifies the socket. This is the same socket that was specified when the overlapped operation was started by a call to 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>, 
<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>, 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>, 
<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>, or 
<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>.


### -param lpOverlapped [in]

Pointer to a 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure that was specified when the overlapped operation was started.


### -param lpcbTransfer [out]

Pointer to a 32-bit variable that receives the number of bytes that were actually transferred by a send or receive operation, or by 
<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>.


### -param fWait [in]

Specifies whether the function should wait for the pending overlapped operation to complete. If <b>TRUE</b>, the function does not return until the operation has been completed. If <b>FALSE</b> and the operation is still pending, the function returns <b>FALSE</b> and <i>lpErrno</i> is WSA_IO_INCOMPLETE. The <i>fWait</i> parameter may be set to <b>TRUE</b> only if the overlapped operation selected event-based completion notification.


### -param lpdwFlags [out]

Pointer to a 32-bit variable that will receive one or more flags that supplement the completion status. If the overlapped operation was initiated through 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a> or 
<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>, this parameter will contain the results value for <i>lpFlags</i> parameter.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If 
<b>WSPGetOverlappedResult</b> succeeds, the return value is <b>TRUE</b>. This means the overlapped operation has completed successfully and the value pointed to by <i>lpcbTransfer</i> has been updated. If 
<b>WSPGetOverlappedResult</b> returns <b>FALSE</b>, this means that the overlapped operation has not completed or the overlapped operation completed but with errors, or completion status could not be determined due to errors in one or more parameters to 
<b>WSPGetOverlappedResult</b>. On failure, the value pointed to by <i>lpcbTransfer</i> will not be updated. The <i>lpErrno</i> parameter indicates the cause of the failure (either of 
<b>WSPGetOverlappedResult</b> or of the associated overlapped operation).

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <b>hEvent</b> member of the 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure does not contain a valid event object handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is unacceptable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_IO_INCOMPLETE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>fWait</i> parameter is <b>FALSE</b> and the I/O operation has not yet completed.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The results reported by the 
<b>WSPGetOverlappedResult</b> function are those of the specified socket's last overlapped operation to which the specified 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure was provided, and for which the operation's results were pending. A pending operation is indicated when the function that started the operation returns SOCKET_ERROR, and the <i>lpErrno</i> is WSA_IO_PENDING. When an I/O operation is pending, the function that started the operation resets the <b>hEvent</b> member of the 
<b>WSAOVERLAPPED</b> structure to the nonsignaled state. Then, when the pending operation has been completed, the system sets the event object to the signaled state.

If the <i>fWait</i> parameter is <b>TRUE</b>, 
<b>WSPGetOverlappedResult</b> determines whether the pending operation has been completed by blocking and waiting for the event object to be in the signaled state. A client may set the <i>fWait</i> parameter to <b>TRUE</b> only if it selected event-based completion notification when the I/O operation was requested. If another form of notification was selected, the usage of the <b>hEvent</b> member of the 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure is different, and setting <i>fWait</i> to <b>TRUE</b> causes unpredictable results.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>
<h3><a id="Interaction_with_WPUCompleteOverlappedRequest"></a><a id="interaction_with_wpucompleteoverlappedrequest"></a><a id="INTERACTION_WITH_WPUCOMPLETEOVERLAPPEDREQUEST"></a>Interaction with WPUCompleteOverlappedRequest</h3>
The behavior of 
<a href="https://msdn.microsoft.com/b0e5015f-d23f-46da-91b1-f646111f70f9">WPUCompleteOverlappedRequest</a> places some constraints on how a service provider implements 
<b>WSPGetOverlappedResult</b> since only the <b>Offset</b> and <b>OffsetHigh</b> members of the 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure are exclusively controlled by the service provider even though three values (byte count, flags, and error) must be retrieved from the structure by 
<b>WSPGetOverlappedResult</b>. A service provider may accomplish this any way it chooses as long as it interacts with the behavior of 
<b>WPUCompleteOverlappedRequest</b> properly. The following description presents a typical implementation:

At the start of overlapped processing, the service provider sets <b>Internal</b> to WSS_OPERATION_IN_PROGRESS.

When the I/O operation is complete, the provider sets <b>OffsetHigh</b> to the Windows Sockets 2 error code resulting from the operation, sets <b>Offset</b> to the flags resulting from the I/O operation, and calls 
<a href="https://msdn.microsoft.com/b0e5015f-d23f-46da-91b1-f646111f70f9">WPUCompleteOverlappedRequest</a>, passing the transfer byte count as one of the parameters. 
<b>WPUCompleteOverlappedRequest</b> eventually sets <b>InternalHigh</b> to the transfer byte count, then sets <b>Internal</b> to a value other than WSS_OPERATION_IN_PROGRESS.

When 
<b>WSPGetOverlappedResult</b> is called, the service provider checks Internal. If it is WSS_OPERATION_IN_PROGRESS, the provider waits on the event handle in the <b>hEvent</b> member or returns an error, based on the setting of the <i>fWait</i> flag of 
<b>WSPGetOverlappedResult</b>. If not in progress, or after completion of waiting, the provider returns the values from <b>InternalHigh</b>, <b>OffsetHigh</b>, and <b>Offset</b> as the transfer count, operation result error code, and flags respectively.




## -see-also




<a href="https://msdn.microsoft.com/b0e5015f-d23f-46da-91b1-f646111f70f9">WPUCompleteOverlappedRequest</a>



<a href="https://msdn.microsoft.com/d73aa3a8-cef5-485d-b2ba-b2fe42ab6200">WSPAccept</a>



<a href="https://msdn.microsoft.com/1daca98e-57d8-47f1-af5f-778a33b2c538">WSPConnect</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>



<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>



<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>



<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>



<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>
 

 

