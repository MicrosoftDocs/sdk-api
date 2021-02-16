---
UID: NS:mswsock._RIO_NOTIFICATION_COMPLETION
title: RIO_NOTIFICATION_COMPLETION (mswsock.h)
description: Specifies the method for I/O completion to be used with a RIONotify function for sending or receiving network data with the Winsock registered I/O extensions.
helpviewer_keywords: ["*PRIO_NOTIFICATION_COMPLETION","PRIO_NOTIFICATION_COMPLETION","PRIO_NOTIFICATION_COMPLETION structure pointer [Winsock]","RIO_NOTIFICATION_COMPLETION","RIO_NOTIFICATION_COMPLETION structure [Winsock]","mswsock/PRIO_NOTIFICATION_COMPLETION","mswsock/RIO_NOTIFICATION_COMPLETION","winsock.rio_notification_completion"]
old-location: winsock\rio_notification_completion.htm
tech.root: WinSock
ms.assetid: 85D3D68F-A914-4126-8D3D-4A6E3F970A4B
ms.date: 12/05/2018
ms.keywords: '*PRIO_NOTIFICATION_COMPLETION, PRIO_NOTIFICATION_COMPLETION, PRIO_NOTIFICATION_COMPLETION structure pointer [Winsock], RIO_NOTIFICATION_COMPLETION, RIO_NOTIFICATION_COMPLETION structure [Winsock], mswsock/PRIO_NOTIFICATION_COMPLETION, mswsock/RIO_NOTIFICATION_COMPLETION, winsock.rio_notification_completion'
req.header: mswsock.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: RIO_NOTIFICATION_COMPLETION, *PRIO_NOTIFICATION_COMPLETION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RIO_NOTIFICATION_COMPLETION
 - mswsock/_RIO_NOTIFICATION_COMPLETION
 - PRIO_NOTIFICATION_COMPLETION
 - mswsock/PRIO_NOTIFICATION_COMPLETION
 - RIO_NOTIFICATION_COMPLETION
 - mswsock/RIO_NOTIFICATION_COMPLETION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mswsock.h
api_name:
 - RIO_NOTIFICATION_COMPLETION
---

# RIO_NOTIFICATION_COMPLETION structure


## -description

The <b>RIO_NOTIFICATION_COMPLETION</b> structure specifies the method for I/O completion to be used with a <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> function for sending or receiving network data with the Winsock registered I/O extensions.

## -struct-fields

### -field Type

The type of completion to use with the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> function when sending or receiving data.

### -field Event

### -field Event.EventHandle

The handle for the event to set following a completed <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> request.

This value is valid when the <b>Type </b> member is set to <b>RIO_EVENT_COMPLETION</b>.

### -field Event.NotifyReset

The boolean value that causes the associated event to be reset when the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> function is called. A non-zero value cause the associated event to be reset. 

This value is valid when the <b>Type </b> member is set to <b>RIO_EVENT_COMPLETION</b>.

### -field Iocp

### -field Iocp.IocpHandle

The handle for the I/O completion port to use for queuing a <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> request completion. 

This value is valid when the <b>Type </b> member is set to <b>RIO_IOCP_COMPLETION</b>.

### -field Iocp.CompletionKey

The value to use for <i>lpCompletionKey</i> parameter returned by the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> or <a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a> function when queuing a <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> request. 

This value is valid when the <b>Type </b> member is set to <b>RIO_IOCP_COMPLETION</b>.

### -field Iocp.Overlapped

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure to use when queuing a <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> request completion.  This member must point to a valid <b>OVERLAPPED</b> structure.  

This value is valid when the <b>Type </b> member is set to <b>RIO_IOCP_COMPLETION</b>.

## -remarks

The <b>RIO_NOTIFICATION_COMPLETION</b> structure is used to specify the behavior of the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> function used with the Winsock registered I/O extensions. 

The <b>RIO_NOTIFICATION_COMPLETION</b> structure is passed to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreatecompletionqueue">RIOCreateCompletionQueue</a> function when a  <a href="/windows/desktop/WinSock/riocqueue">RIO_CQ</a> is created. If an application does not call the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> function for a completion queue, the completion queue can be created without a <b>RIO_NOTIFICATION_COMPLETION</b> object.

For completion queues using an event, the <b>Type</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> structure is set to <b>RIO_EVENT_COMPLETION</b>. The <b>Event.EventHandle</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> structure should contain the handle for an event created by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function.  To receive the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> completion, the application should wait on the specified event handle using <a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> or a similar wait routine.  If the application plans to reset and reuse the event, the application can reduce overhead by setting the <b>Event.NotifyReset</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> structure to a non-zero value. This causes the event to be reset by the <b>RIONotify</b> function when notification occurs. This mitigates the need to call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaresetevent">WSAResetEvent</a> function to reset the event between calls to the <b>RIONotify</b> function.  

For completion queues using an I/O completion port, the <b>Type</b> member  of the <b>RIO_NOTIFICATION_COMPLETION</b> structure is set to <b>RIO_IOCP_COMPLETION</b>. The <b>Iocp.IocpHandle</b> member  of the <b>RIO_NOTIFICATION_COMPLETION</b> structure should contain the handle for an I/O completion port created by the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function.  To receive the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> completion, the application should call the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> or <a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a> function.  The application should provide a dedicated <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> object for the completion queue, and it may also use the <b>Iocp.CompletionKey</b> member to distinguish <b>RIONotify</b> requests on the completion queue from other I/O completions including <b>RIONotify</b> completions for other completion queues.



An application using thread pools can use thread pool wait objects to get <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a> completions via its thread pool.  In that case, the call to the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a> function should immediately follow the call to <b>RIONotify</b>.  If the <b>SetThreadpoolWait</b> function is called before <b>RIONotify</b> and the application relies on <b>RIONotify</b> to clear the event object, this may result in spurious executions of the wait object callback.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreatecompletionqueue">RIOCreateCompletionQueue</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify">RIONotify</a>



<a href="/windows/desktop/WinSock/riocqueue">RIO_CQ</a>



<a href="/windows/desktop/api/mswsock/ne-mswsock-rio_notification_completion_type">RIO_NOTIFICATION_COMPLETION_TYPE</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacreateevent">WSACreateEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaresetevent">WSAResetEvent</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>