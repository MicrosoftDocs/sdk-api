---
UID: NF:winsock2.SocketNotificationRetrieveEvents
title: SocketNotificationRetrieveEvents
description: This inline helper function is provided as a convenience to retrieve the events mask from an [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry).
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
 - SocketNotificationRetrieveEvents
f1_keywords:
 - SocketNotificationRetrieveEvents
 - winsock2/SocketNotificationRetrieveEvents
dev_langs:
 - c++
---

## -description

This inline helper function is provided as a convenience to retrieve the events mask from an [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry).

For more info, and code examples, see [Winsock socket state notifications](/windows/win32/winsock/winsock-socket-state-notifications).

## -parameters

### -param notification

Type: \_In\_ **[OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry)\***

A pointer to an [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry) received for a socket state notification.

## -returns

A [UINT32](/windows/win32/winprog/windows-data-types) containing a bitmask of the notification events for the socket.

This table lists the socket notification events. These are the events possible when a notification is received.

|Event|Description|
|-|-|
|SOCK_NOTIFY_EVENT_IN|Input is available from the socket without blocking.|
|SOCK_NOTIFY_EVENT_OUT|Output can be provided to the socket without blocking.|
|SOCK_NOTIFY_EVENT_HANGUP|The socket connection has terminated.|
|SOCK_NOTIFY_EVENT_ERR|The socket is in an error state.|
|SOCK_NOTIFY_EVENT_REMOVE|The notification has been deregistered.|

## -remarks

The **SOCK_NOTIFY_EVENT_ERR** and **SOCK_NOTIFY_EVENT_REMOVE** events might be indicated regardless of registered event filter.

If a **SOCK_NOTIFY_EVENT_REMOVE** event is indicated, then no more notifications will be provided.

## -see-also

* [OVERLAPPED_ENTRY](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry)
* [ProcessSocketNotifications](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications)
* [Winsock socket state notifications](/windows/win32/winsock/winsock-socket-state-notifications)
