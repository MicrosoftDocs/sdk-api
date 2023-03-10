---
UID: NF:winsock2.ProcessSocketNotifications
title: ProcessSocketNotifications
description: Associates a set of sockets with a completion port, and retrieves any notifications that are already pending on that port. Once associated, the completion port receives the socket state notifications that were specified.
ms.date: 11/17/2020
tech.root: WinSock
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Ws2_32.dll
req.header: winsock2.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Ws2_32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
 - wsock32.dll
api_name:
 - ProcessSocketNotifications
f1_keywords:
 - ProcessSocketNotifications
 - winsock2/ProcessSocketNotifications
dev_langs:
 - c++
---

## -description

Associates a set of sockets with a completion port, and retrieves any notifications that are already pending on that port. Once associated, the completion port receives the socket state notifications that were specified. Only Microsoft [Winsock](/windows/win32/winsock/windows-sockets-start-page-2) provider sockets are supported.

To reduce system call overhead, you can register for notifications and retrieve them in a single call to **ProcessSocketNotifications**. Alternatively, you can retrieve them explicitly by calling the usual I/O completion port functions, such as [GetQueuedCompletionStatus](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus). Notifications retrieved using **ProcessSocketNotifications** are the same as those retrieved using [GetQueuedCompletionStatusEx](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex), which might include notification packets other than socket state changes.

The notification event flags are the integer value of the *dwNumberOfBytesTransferred* fields of the returned [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry) structures. This is similar to using [JOBOBJECT_ASSOCIATE_COMPLETION_PORT](/windows/win32/api/winnt/ns-winnt-jobobject_associate_completion_port), which also uses the *dwNumberOfBytesTransferred* field to send integer messages. Call the [SocketNotificationRetrieveEvents](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) function to obtain them.

A socket handle can be registered to only one IOCP at a time. Re-registering a previously-registered socket handle overwrites the existing registration. Before you close a handle used for registration, you should explicitly remove registration, and wait for the **SOCK_NOTIFY_EVENT_REMOVE** notification (see **Remarks** in this topic).

For more info, and code examples, see [Winsock socket state notifications](/windows/win32/winsock/winsock-socket-state-notifications).

## -parameters

### -param completionPort

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an I/O completion port created using the [CreateIoCompletionPort](/windows/win32/fileio/createiocompletionport) function. The port will be used in the *CompletionPort* parameter of the [PostQueuedCompletionStatus](/windows/win32/fileio/postqueuedcompletionstatus) function when messages are sent on behalf of the socket.

### -param registrationCount

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of registrations supplied by *registrationInfos*.

### -param registrationInfos

Type: \_Inout\_updates\_opt\_(registrationCount) **[SOCK_NOTIFY_REGISTRATION](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)\***

A pointer to an array of [SOCK_NOTIFY_REGISTRATION](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration) structures that define the notification registration parameters. These include the socket of interest, the notification events of interest, and the operation flags. On success, you must inspect the elements for whether the registration was processed successfully. This argument must be **NULL** if *registrationCount* is 0.

### -param timeoutMs

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

The time in milliseconds that you're willing to wait for a completion packet to appear at the completion port. If a completion packet doesn't appear within the specified time, then the function times out and returns **ERROR_TIMEOUT**.

If *timeoutMs* is **INFINITE** (0xFFFFFFFF), then the function will never time out. If *timeoutMs* is 0, and there is no I/O operation to dequeue, then the function will time out immediately.

The value of *timeoutMs* must be 0 if *completionCount* is 0.

### -param completionCount

Type: \_In\_ **[ULONG](/windows/win32/winprog/windows-data-types)**

The maximum number of [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry) structures to remove. If 0 is specified, then only registration operations will be processed. 

### -param completionPortEntries

Type: \_Out\_writes\_to\_opt\_(completionCount, *receivedEntryCount) **[OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry)\***

On input, points to a pre-allocated array of [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry) structures. The array mustn't overlap with the *registrationInfos* array. The value of *completionPortEntries* must be **NULL** if *completionCount* is 0.

On output, receives an array of OVERLAPPED_ENTRY structures that hold the entries. The number of array elements is provided by ReceivedEntryCount. The dwNumberOfBytesTransferred fields of the structures are integer masks of received events. The lpOverlapped fields are reserved and must not be used as pointers.

### -param receivedEntryCount

Type: \_Out\_opt\_ **[UINT32](/windows/win32/winprog/windows-data-types)\***

A pointer to a variable that receives the number of entries removed. Must be **NULL** if *completionCount* is 0.

## -returns

If successful, returns **ERROR_SUCCESS**. If the function succeeded and you supplied a non-0 *completionCount*, but no completion packets appeared within the specified time, returns **WAIT_TIMEOUT**. Otherwise, returns an appropriate **WSAE\*** error code.

If **ERROR_SUCCESS** or **WAIT_TIMEOUT** is returned, then you must inspect the individual registration infos' registration results. Otherwise, the entire operation failed, and no changes occurred.

## -remarks

See [SocketNotificationRetrieveEvents](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) for the events that are possible when a notification is received.

## -see-also

* [CreateIoCompletionPort](/windows/win32/fileio/createiocompletionport)
* [GetQueuedCompletionStatus](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
* [GetQueuedCompletionStatusEx](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
* [JOBOBJECT_ASSOCIATE_COMPLETION_PORT](/windows/win32/api/winnt/ns-winnt-jobobject_associate_completion_port)
* [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry)
* [PostQueuedCompletionStatus](/windows/win32/fileio/postqueuedcompletionstatus)
* [SOCK_NOTIFY_REGISTRATION](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)
* [SocketNotificationRetrieveEvents](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents)
* [Winsock](/windows/win32/winsock/windows-sockets-start-page-2)
* [Winsock socket state notifications](/windows/win32/winsock/winsock-socket-state-notifications)
