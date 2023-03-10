---
UID: NS:winsock2.SOCK_NOTIFY_REGISTRATION
title: SOCK_NOTIFY_REGISTRATION
description: Represents info supplied to the [ProcessSocketNotifications](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) function.
targetos: Windows
tech.root: WinSock
ms.date: 11/17/2020
req.construct-type: structure
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: SOCK_NOTIFY_REGISTRATION
req.redist: 
f1_keywords:
 - SOCK_NOTIFY_REGISTRATION
 - winsock2/SOCK_NOTIFY_REGISTRATION
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winsock2.h
api_name:
 - SOCK_NOTIFY_REGISTRATION
---

## -description

Represents info supplied to the [ProcessSocketNotifications](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) function.

For more info, and code examples, see [Winsock socket state notifications](/windows/win32/winsock/winsock-socket-state-notifications).

## -struct-fields

### -field socket

Type: **SOCKET**

A handle to a Winsock socket opened by any of the [WSASocket](/windows/win32/api/winsock2/nf-winsock2-wsasocketw), [socket](/windows/win32/api/winsock2/nf-winsock2-socket), [WSAAccept](/windows/win32/api/winsock2/nf-winsock2-wsaaccept), [accept](/windows/win32/api/winsock2/nf-winsock2-accept), or [WSADuplicateSocket](/windows/win32/api/winsock2/nf-winsock2-wsaduplicatesocketw) functions. Only Microsoft [Winsock](/windows/win32/winsock/windows-sockets-start-page-2) provider sockets are supported.

### -field completionKey

Type: **PVOID**

The value to use in the *dwCompletionKey* parameter of the [PostQueuedCompletionStatus](/windows/win32/fileio/postqueuedcompletionstatus) function when notifications are sent on behalf of the socket. This parameter is used upon registration creation. To change the completion key, remove the registration and re-register it.

### -field eventFilter

Type: **[UINT16](/windows/win32/winprog/windows-data-types)**

A set of flags indicating the notifications being requested. This must be one or more of the following values (defined in `WinSock2.h`).

**SOCK_NOTIFY_REGISTER_EVENT_NONE**. Notifications should not be issued.
**SOCK_NOTIFY_REGISTER_EVENT_IN**. A notification should be issued when data can be read without blocking.
**SOCK_NOTIFY_REGISTER_EVENT_OUT**. A notification should be issued when data can be written without blocking.
**SOCK_NOTIFY_REGISTER_EVENT_HANGUP**. A notification should be issued when a stream-oriented connection was either disconnected or aborted.
**SOCK_NOTIFY_REGISTER_EVENTS_ALL**. Has the value `(SOCK_NOTIFY_REGISTER_EVENT_IN | SOCK_NOTIFY_REGISTER_EVENT_OUT | SOCK_NOTIFY_REGISTER_EVENT_HANGUP)`.

### -field operation

Type: **[UINT8](/windows/win32/winprog/windows-data-types)**

Indicates the operation to perform on a registration. At most one operation may be performed at a time. These values are defined in `WinSock2.h`.

**SOCK_NOTIFY_OP_NONE**. No registration operations should take place. Use this if your application calls [ProcessSocketNotifications](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) and is only interested in receiving notifications.
**SOCK_NOTIFY_OP_ENABLE**. Enables the registration. Notifications must not be re-enabled until the **SOCK_NOTIFY_EVENT_DISABLE** notification is received. 
**SOCK_NOTIFY_OP_DISABLE**. Disables the registration, but doesn't destroy the underlying data structures. Note that this doesn't remove the registration, it merely suppresses queuing of new notifications. Notifications that have already been queued might still be delivered until the **SOCK_NOTIFY_EVENT_DISABLE** event is received. 
**SOCK_NOTIFY_OP_REMOVE**. Removes a previously-registered notification. Both enabled and disabled notifications may be removed. The **SOCK_NOTIFY_EVENT_REMOVE** notification is issued, with the guarantee that no more notifications will be issued afterwards for that completion key unless it is re-registered.

### -field triggerFlags

Type: **[UINT8](/windows/win32/winprog/windows-data-types)**

A set of flags indicating the trigger behavior (defined in `WinSock2.h`).

**SOCK_NOTIFY_TRIGGER_ONESHOT**. The registration will be disabled (not removed) upon delivery of the next notification.
**SOCK_NOTIFY_TRIGGER_PERSISTENT**. The registration will remain active until it is explicitly disabled or removed.
**SOCK_NOTIFY_TRIGGER_LEVEL**. The registration is for level-triggered notifications. Not compatible with edge-triggered. One of edge- or level-triggered must be supplied.
**SOCK_NOTIFY_TRIGGER_EDGE**. The registration is for edge-triggered notifications. Not compatible with level-triggered. One of edge- or level-triggered must be supplied.

Notifications are only supplied when the registration is enabled. Notifications are not queued up while the registration is disabled. As notifications are queued up for a given socket, they are coalesced into a single notification. Therefore, multiple events may be described by a single event mask for the socket.

Given the registration is enabled, level-triggered notifications are supplied whenever the desired conditions hold.

Given the registration is enabled, edge-triggered notifications are supplied whenever a condition changes from not holding to holding. The condition must change while the registration is enabled for a notification to be queued. As such, after registering, the socket's receive buffer must be completely drained to ensure a notification is received.

### -field registrationResult

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

After a successful call to [ProcessSocketNotifications](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications), *registrationResult* contains a code indicating the success or failure of the registration. A value of **ERROR_SUCCESS** indicates that registration was successful.

## -remarks

## -see-also

* [accept](/windows/win32/api/winsock2/nf-winsock2-accept)
* [PostQueuedCompletionStatus](/windows/win32/fileio/postqueuedcompletionstatus)
* [ProcessSocketNotifications](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications)
* [socket](/windows/win32/api/winsock2/nf-winsock2-socket)
* [Winsock](/windows/win32/winsock/windows-sockets-start-page-2)
* [Winsock socket state notifications](/windows/win32/winsock/winsock-socket-state-notifications)
* [WSAAccept](/windows/win32/api/winsock2/nf-winsock2-wsaaccept)
* [WSADuplicateSocket](/windows/win32/api/winsock2/nf-winsock2-wsaduplicatesocketw)
* [WSASocket](/windows/win32/api/winsock2/nf-winsock2-wsasocketw)
