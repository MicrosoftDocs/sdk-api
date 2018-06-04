---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _OVERLAPPED structure


## -description


Contains information used in asynchronous (overlapped) input/output (I/O).


## -struct-fields




### -field Internal

Type: <b>ULONG_PTR</b>

Reserved for operating system use. This member, which specifies a system-dependent status, is valid when the <a href="https://msdn.microsoft.com/5a53934f-bbff-4bb0-b374-01adb629a041">IStreamAsync::OverlappedResult</a> function returns without setting the extended error information to <b>ERROR_IO_PENDING</b>.


### -field InternalHigh

Type: <b>ULONG_PTR</b>

Reserved for operating system use. This member, which specifies the length of the data transferred, is valid when the <a href="https://msdn.microsoft.com/5a53934f-bbff-4bb0-b374-01adb629a041">IStreamAsync::OverlappedResult</a> function returns <b>TRUE</b>.


### -field Offset

Type: <b>DWORD</b>

File position at which to start the transfer. The file position is a byte offset from the start of the file. The calling process must set this member before it calls the <a href="https://msdn.microsoft.com/c0046a89-1427-465e-a5f3-2398ebff04f3">IStreamAsync::ReadAsync</a> or <a href="https://msdn.microsoft.com/c5004923-191b-4ec1-83af-f066209c786a">IStreamAsync::WriteAsync</a> function.


### -field OffsetHigh

Type: <b>DWORD</b>

High-order word of the file position at which to start the transfer.


### -field Pointer

Type: <b>PVOID</b>

Reserved.


### -field hEvent

Type: <b>handle</b>

Handle to an event that is set to the signaled state when the operation has been completed. The calling process must set this member either to zero or a valid event handle before it calls any overlapped functions. To create an event object, use the <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. This function returns a handle that can be used to synchronize simultaneous I/O requests for a device.

Functions such as <a href="https://msdn.microsoft.com/c0046a89-1427-465e-a5f3-2398ebff04f3">IStreamAsync::ReadAsync</a> and <a href="https://msdn.microsoft.com/c5004923-191b-4ec1-83af-f066209c786a">IStreamAsync::WriteAsync</a> set this handle to the nonsignaled state before they begin an I/O operation. When the operation has completed, the handle is set to the signaled state.

Functions such as <a href="https://msdn.microsoft.com/5a53934f-bbff-4bb0-b374-01adb629a041">IStreamAsync::OverlappedResult</a> and the wait functions reset auto-reset events to the nonsignaled state. Therefore, if an auto-reset event is used, the application can stop responding if it waits for the operation to complete and then calls <b>IStreamAsync::OverlappedResult</b>.


## -remarks



This structure should always be initialized to zero before it is used in a function call. If it is not, the function can fail and return <b>ERROR_INVALID_PARAMETER</b>.

 Use the <a href="https://msdn.microsoft.com/ca2a1c59-b538-4c1b-9ad3-89d00f19325d">IStreamAsync::CancelIo</a> function to cancel an asynchronous I/O operation.

A common mistake is to reuse an <b>OVERLAPPED</b> structure before the previous asynchronous operation has been completed. Use a separate structure for each request. Create an event object for each thread that processes data. 



