---
UID: NC:mswsock.LPFN_RIOCREATECOMPLETIONQUEUE
title: LPFN_RIOCREATECOMPLETIONQUEUE
author: windows-sdk-content
description: Creates an I/O completion queue of a specific size for use with the Winsock registered I/O extensions.
old-location: 
tech.root: WinSock
ms.assetid: A5700ACD-3F4B-4AFF-8BA1-6AC59402E06C
ms.author: windowssdkdev
ms.date: 01/30/19
ms.keywords: LPFN_RIOCREATECOMPLETIONQUEUE
ms.topic: language-reference
targetos: Windows
product: Windows
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
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mswsock.h
api_name:
 - LPFN_RIOCREATECOMPLETIONQUEUE
---

## -description

The **RIOCreateCompletionQueue** function creates an I/O completion queue of a specific size for use with the Winsock registered I/O extensions.


## -parameters

### -param QueueSize

The size, in number of entries, of the completion queue to create.


### -param NotificationCompletion

The type of notification completion to use based on the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](rio-notification-completion.md) structure (I/O completion or event notification).

If the **Type** member is set to **RIO\_EVENT\_COMPLETION**, then the **Event** member of the [**RIO\_NOTIFICATION\_COMPLETION**](rio-notification-completion.md) structure must be set.

If the **Type** member is set to **RIO\_IOCP\_COMPLETION**, then the **Iocp** member of the [**RIO\_NOTIFICATION\_COMPLETION**](rio-notification-completion.md) structure must be set and the **Iocp.Overlapped** member of the **RIO\_NOTIFICATION\_COMPLETION** structure must not be NULL.

If the *NotificationCompletion* parameter is NULL, this specifies no notification completion is used and that polling must be used to determine completion.

## -returns

If no error occurs, the **RIOCreateCompletionQueue** function returns a descriptor referencing a new completion queue. Otherwise, a value of **RIO\_INVALID\_CQ** is returned, and a specific error code can be retrieved by calling the [**WSAGetLastError**](wsagetlasterror-2.md) function.

| Return code                                                                                                                               | Description                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md#wsaefault)**</dt> </dl>   | The system detected an invalid pointer address in attempting to use a pointer argument in a call.<br/>                                                                                                                 |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md#wsaeinval)**</dt> </dl>   | An invalid parameter was passed to the function. <br/> This error is returned if the *QueueSize* parameter is less than 1 or greater than **RIO\_MAX\_CQ\_SIZE** defined in the *Mswsockdef.h* header file.<br/> |
| <dl> <dt>**[WSAENOBUFS](windows-sockets-error-codes-2.md#wsaenobufs)**</dt> </dl> | Sufficient memory could not be allocated. This error is returned if there was insufficient memory to allocate the completion queue requested based on the *QueueSize* parameter. <br/>                                 |


## -remarks

The **RIOCreateCompletionQueue** function creates an I/O completion queue of a specific size. The size of the completion queue restricts the set of registered I/O sockets that can be associated with the completion queue. For more information, see the [**RIOCreateRequestQueue**](riocreaterequestqueue.md) function.

When creating a [**RIO\_CQ**](riocqueue.md), the [**RIO\_NOTIFICATION\_COMPLETION**](rio-notification-completion.md) structure pointed to by the *NotificationCompletion* parameter determines how the application will receive completion queue notifications. If a **RIO\_NOTIFICATION\_COMPLETION** structure is provided when creating the completion queue, the application may call the [**RIONotify**](rionotify.md) function to request a completion queue notification. Normally this notification occurs when the completion queue is not empty. This may happen immediately or when the next completion entry is inserted into the completion queue. However, send and receive requests may be flagged as **RIO\_MSG\_DONT\_NOTIFY**. Completion queue notification and will never be triggered as a result of such requests. If the completion queue contains only entries with the **RIO\_MSG\_DONT\_NOTIFY** flag set, the completion queue notification will not be triggered. Also, when a new entry enters the completion queue, the completion queue notification is only triggered if the **RIO\_MSG\_DONT\_NOTIFY** flag was not set on the associated request. Any completed requests can still be retrieved by polling using the [**RIODequeueCompletion**](riodequeuecompletion.md) function. Once a completion queue notification is issued, the application must call the **RIONotify** function in order to receive another completion queue notification. When a completion queue notification occurs, the application typically calls the **RIODequeueCompletion** function to dequeue the completed send or receive requests.

Two options are available for completion queue notification.

-   Event handles.
-   I/O completion ports

If the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](rio-notification-completion.md) structure is set to **RIO\_EVENT\_COMPLETION**, an event handle is used to signal completion queue notifications. An event handle is provided as the **EventNotify.EventHandle** member in the **RIO\_NOTIFICATION\_COMPLETION** structure passed to the **RIOCreateCompletionQueue** function. The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](wsacreateevent-2.md) or [**CreateEvent**](base.createevent) function. To receive the [**RIONotify**](rionotify.md) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](wsawaitformultipleevents-2.md) or a similar wait routine. The completion of the **RIONotify** function for this [**RIO\_CQ**](riocqueue.md) will signal the event. The **Event.NotifyReset** member in the **RIO\_NOTIFICATION\_COMPLETION** structure passed to the **RIOCreateCompletionQueue** function indicates whether or not the event should be reset as part of a call to the **RIONotify** function. If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value. This causes the event to be automatically reset by the **RIONotify** function when the notification occurs. This mitigates the need to call the [**WSAResetEvent**](wsaresetevent-2.md) function to reset the event between calls to the **RIONotify** function.

If the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](rio-notification-completion.md) structure is set to **RIO\_IOCP\_COMPLETION**, an I/O completion port is used to signal completion queue notifications. An I/O completion port handle is provided as the **Iocp.IocpHandle** member in the **RIO\_NOTIFICATION\_COMPLETION** structure passed to the **RIOCreateCompletionQueue** function. The completion of the [**RIONotify**](rionotify.md) function for this [**RIO\_CQ**](riocqueue.md) will queue an entry to the I/O completion port which can be retrieved using the [**GetQueuedCompletionStatus**](fs.getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](fs.getqueuedcompletionstatusex_func) function. A queued entry will have the returned *lpCompletionKey* parameter value set to the value specified in **Iocp.CompletionKey** member of the **RIO\_NOTIFICATION\_COMPLETION** structure and the **Iocp.Overlapped** member in the **RIO\_NOTIFICATION\_COMPLETION** structure will be a non-NULL value.

In terms of its usage, completion queue notification is designed to wake up a waiting application thread so that the thread can examine the completion queue. Waking and scheduling a thread comes at a cost, so if this happens too frequently it will have a negative impact on the application performance. The **RIO\_MSG\_DONT\_NOTIFY** flag is provided so that the application can control the frequency of these events and limit their over impact on performance.

> [!Note]  
> For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives. If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism. This locking is not needed for access by a single thread. Different threads can access separate requests/completion queues without locks. The need for synchronization occurs only when multiple threads try to access the same queue. Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.

 

> [!Note]  
> The function pointer to the **RIOCreateCompletionQueue** function must be obtained at run time by making a call to the [**WSAIoctl**](wsaioctl-2.md) function with the **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** opcode specified. The input buffer passed to the **WSAIoctl** function must contain **WSAID\_MULTIPLE\_RIO**, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O extension functions. On success, the output returned by the **WSAIoctl** function contains a pointer to the [**RIO\_EXTENSION\_FUNCTION\_TABLE**](rio-extension-function-table.md) structure that contains pointers to the Winsock registered I/O extension functions. The **SIO\_GET\_MULTIPLE\_EXTENSION\_FUNCTION\_POINTER** IOCTL is defined in the *Ws2def.h* header file. The **WSAID\_MULTIPLE\_RIO** GUID is defined in the *Mswsock.h* header file.

 

**Windows Phone 8:** This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

**Windows 8.1** and **Windows Server 2012 R2**: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

