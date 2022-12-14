---
UID: NC:mswsock.LPFN_RIORESIZEREQUESTQUEUE
title: LPFN_RIORESIZEREQUESTQUEUE
description: Resizes a request queue to be either larger or smaller for use with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIORESIZEREQUESTQUEUE"]
old-location: 
tech.root: WinSock
ms.assetid: 4A20B1E3-ED99-4429-A9C1-35C9330CB108
ms.date: 01/30/2019
ms.keywords: LPFN_RIORESIZEREQUESTQUEUE
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mswsock.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - LPFN_RIORESIZEREQUESTQUEUE
 - mswsock/LPFN_RIORESIZEREQUESTQUEUE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIORESIZEREQUESTQUEUE
---

## -description

The **RIOResizeRequestQueue** function resizes a request queue to be either larger or smaller for use with the Winsock registered I/O extensions.

## -parameters

### -param RQ

A descriptor that identifies an existing registered I/O socket descriptor (request queue) to resize.

### -param MaxOutstandingReceive

The maximum number of outstanding sends allowed on the socket. This value can be larger or smaller than the original number.

This parameter is usually a small number for most applications.

### -param MaxOutstandingSend

The maximum number of outstanding receives allowed on the socket. This value can be larger or smaller than the original number.

## -returns

If no error occurs, the **RIOResizeRequestQueue** function returns **TRUE**. Otherwise, a value of **FALSE** is returned, and a specific error code can be retrieved by calling the [**WSAGetLastError**](../winsock/nf-winsock-wsagetlasterror.md) function.



| Return code                                                                                                                                         | Description                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSAEINVAL](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeinval)**</dt> </dl>             | An invalid parameter was passed to the function. This error is returned if the *RQ* parameter is not valid (RIO\_INVALID\_RQ, for example). This error is also returned if both the *MaxOutstandingReceive* and *MaxOutstandingSend* parameters are zero. <br/> |
| <dl> <dt>**[WSAENOBUFS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaenobufs)**</dt> </dl>           | Sufficient memory could not be allocated. This error is returned if memory could not be allocated for the resized request queue.<br/>                                                                                                                           |
| <dl> <dt>**[WSAETOOMANYREFS](/windows/win32/winsock/windows-sockets-error-codes-2#wsaetoomanyrefs)**</dt> </dl> | There are too many operations that still reference the request queue. Resizing of this request queue to be smaller is not possible at this time.<br/>                                                                                                           |

## -remarks

The **RIOResizeRequestQueue** function resizes a request queue to be either larger or smaller. If the request queue already contains entries, those entries will be copied over to the new request queue.

A request queue has a required minimum size that is dependent on the current number of entries (number of sends and receives on the request queue). If an application calls the **RIOResizeRequestQueue** function and tries to set the queue too small for the number of existing entries, the call will fail and the queue will not be resized.

> [!Note]  
> The function pointer to the **RIOResizeRequestQueue** function must be obtained at run time by making a call to the [**WSAIoctl**](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## Thread Safety

If multiple threads attempt to access the same [**RIO\_RQ**](/windows/win32/winsock/riorqueue) using the [**RIODequeueCompletion**](./nc-mswsock-lpfn_riodequeuecompletion.md) or **RIOResizeRequestQueue** function, access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism. If the completion queues are not shared, mutual exclusion is not required.

## -see-also