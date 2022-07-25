---
UID: NC:mswsock.LPFN_RIODEQUEUECOMPLETION
title: LPFN_RIODEQUEUECOMPLETION
description: Removes entries from an I/O completion queue for use with the Winsock registered I/O extensions.
helpviewer_keywords: ["LPFN_RIODEQUEUECOMPLETION"]
old-location: 
tech.root: WinSock
ms.assetid: 658729C0-2963-45F0-B616-01372A7144D1
ms.date: 01/30/2019
ms.keywords: LPFN_RIODEQUEUECOMPLETION
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
 - LPFN_RIODEQUEUECOMPLETION
 - mswsock/LPFN_RIODEQUEUECOMPLETION
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIODEQUEUECOMPLETION
---

## -description

The **RIODequeueCompletion** function removes entries from an I/O completion queue for use with the Winsock registered I/O extensions.

## -parameters

### -param CQ

A descriptor that identifies an I/O completion queue.

### -param Array

An array of [**RIORESULT**](../mswsockdef/ns-mswsockdef-rioresult.md) structures to receive the description of the completions dequeued.

### -param ArraySize

The maximum number of entries in the *Array* to write.

## -returns

If no error occurs, the **RIODequeueCompletion** function returns the number of completion entries removed from the specified completion queue. Otherwise, a value of **RIO\_CORRUPT\_CQ** is returned to indicate that the state of the [**RIO\_CQ**](/windows/win32/winsock/riocqueue) passed in the *CQ* parameter has become corrupt due to memory corruption or misuse of the RIO functions.

## -remarks

The **RIODequeueCompletion** function removes entries from an I/O completion queue for send and receive requests with the Winsock registered I/O extensions.

The **RIODequeueCompletion** function is the mechanism by which an application can find out about completed send and receive requests. An application normally calls the **RIODequeueCompletion** function after receiving notification based on the method registered with the [**RIONotify**](./nc-mswsock-lpfn_rionotify.md) function when the completion queue is not empty. The notification behavior for an I/O completion queue is set when the [**RIO\_CQ**](/windows/win32/winsock/riocqueue) is created. The [**RIO\_NOTIFICATION\_COMPLETION**](./ns-mswsock-rio_notification_completion.md) structure that determines the notification behavior is passed to the [**RIOCreateCompletionQueue**](./nc-mswsock-lpfn_riocreatecompletionqueue.md) function when a **RIO\_CQ** is created.

When the **RIODequeueCompletion** function completes, the *Array* parameter contains an array of pointers to [**RIORESULT**](../mswsockdef/ns-mswsockdef-rioresult.md) structures for the completed send and receive requests that were dequeued. The members of the returned **RIORESULT** structures provide information on the completion status of the completed request and the number of bytes that were transferred. Each returned **RIORESULT** structure also includes a socket context and an application context that can be used to identify the specific completed request.

If the I/O completion queue passed in the *CQ* parameter is not valid or damaged, the **RIODequeueCompletion** function returns a count of **RIO\_CORRUPT\_CQ**.

The **RIODequeueCompletion** function returns a value of zero is returned if there are no completed send or receive requests to be dequeued.

Only after a request’s completion has been dequeued does the system release the association to its buffer and buffer registration, along with its quota charge.

> [!Note]  
> For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](/windows/win32/winsock/riocqueue) structs) and request queues ([**RIO\_RQ**](/windows/win32/winsock/riorqueue) structs) are not protected by synchronization primitives. If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism. This locking is not needed for access by a single thread. Different threads can access separate requests/completion queues without locks. The need for synchronization occurs only when multiple threads try to access the same queue. Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.

 

> [!Note]  
> The function pointer to the **RIODequeueCompletion** function must be obtained at run time by making a call to the [WSAIoctl](../winsock2/nf-winsock2-wsaioctl.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](./ns-mswsock-rio_extension_function_table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## Thread Safety

If multiple threads attempt to access the same [**RIO\_CQ**](/windows/win32/winsock/riocqueue) using the **RIODequeueCompletion** function, access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism. If the completion queues are not shared, mutual exclusion is not required.

## -see-also