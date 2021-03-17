---
UID: NS:rpcasync._RPC_ASYNC_NOTIFICATION_INFO
title: RPC_ASYNC_NOTIFICATION_INFO (rpcasync.h)
description: Contains notification information for asynchronous remote procedure calls. This notification information can be configured for I/O completion ports (IOC), Windows asynchronous procedure calls (APC), Windows messaging, and Windows event notification.
helpviewer_keywords: ["*PRPC_ASYNC_NOTIFICATION_INFO","PRPC_ASYNC_NOTIFICATION_INFO","PRPC_ASYNC_NOTIFICATION_INFO union pointer [RPC]","RPC_ASYNC_NOTIFICATION_INFO","RPC_ASYNC_NOTIFICATION_INFO union [RPC]","rpc.rpc_async_notification_info","rpcasync/PRPC_ASYNC_NOTIFICATION_INFO","rpcasync/RPC_ASYNC_NOTIFICATION_INFO"]
old-location: rpc\rpc_async_notification_info.htm
tech.root: Rpc
ms.assetid: 253f3d23-4cc2-44b3-9d25-c7f26d73ed1e
ms.date: 12/05/2018
ms.keywords: '*PRPC_ASYNC_NOTIFICATION_INFO, PRPC_ASYNC_NOTIFICATION_INFO, PRPC_ASYNC_NOTIFICATION_INFO union pointer [RPC], RPC_ASYNC_NOTIFICATION_INFO, RPC_ASYNC_NOTIFICATION_INFO union [RPC], rpc.rpc_async_notification_info, rpcasync/PRPC_ASYNC_NOTIFICATION_INFO, rpcasync/RPC_ASYNC_NOTIFICATION_INFO'
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: RPC_ASYNC_NOTIFICATION_INFO, *PRPC_ASYNC_NOTIFICATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_ASYNC_NOTIFICATION_INFO
 - rpcasync/_RPC_ASYNC_NOTIFICATION_INFO
 - PRPC_ASYNC_NOTIFICATION_INFO
 - rpcasync/PRPC_ASYNC_NOTIFICATION_INFO
 - RPC_ASYNC_NOTIFICATION_INFO
 - rpcasync/RPC_ASYNC_NOTIFICATION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_ASYNC_NOTIFICATION_INFO
---

# RPC_ASYNC_NOTIFICATION_INFO structure


## -description

The <b>RPC_ASYNC_NOTIFICATION_INFO</b> union  contains notification information for asynchronous remote procedure calls. This notification information can be configured for I/O completion ports (IOC), Windows asynchronous procedure calls (APC), Windows messaging, and Windows event notification.

## -struct-fields

### -field APC

Structure used for Windows asynchronous procedure call (APC) notifications.

### -field APC.NotificationRoutine

Calls the user-defined APC notification routine.

### -field APC.hThread

Handle to the thread on which the notification APC should be posted. A value of zero indicates the current thread.

### -field IOC

Structure used for notification on an I/O completion port.

### -field IOC.hIOPort

Handle to the I/O completion port.

### -field IOC.dwNumberOfBytesTransferred

Set by the RPC client before the asynchronous call is started. When the notification is delivered to the completion port, this value is filled in the location pointed to by the <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

### -field IOC.dwCompletionKey

Set by the RPC client before the asynchronous call is started. When the notification is delivered to the completion port, this value is filled in the location pointed to by the <i>lpCompletionKey</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

### -field IOC.lpOverlapped

Set by the RPC client before the asynchronous call is started. When the notification is delivered to the completion port, this value is filled in the location pointed to by the <i>lpOverlapped</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

### -field HWND

Fields used for notification by a Windows message. When the RPC run time posts the message, <b>wParam</b> is zero, and <b>lParam</b> points to the asynchronous handle for the call (the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>).

<b>Windows Server 2003 or later:  </b>Notification via the HWND is deprecated. Do not use this member.

### -field HWND.hWnd

Identifies the window to which the message should be posted.

### -field HWND.Msg

Message to be posted.

### -field hEvent

Handle used for notification by an event.

### -field Event

### -field NotificationRoutine

Windows Vista or earlier versions of Windows: COM uses this internally for direct callbacks. Do not use this member.

Windows 7 or later versions of Windows: An optional function pointer to a user-defined notification scheme built on top of RPC call completion. As an example, an application could call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a> from the notification callback.

<div class="alert"><b>Note</b>  Making additional RPC calls, blocking,  or performing long running work from notification callbacks is strongly discouraged.</div>
<div> </div>

## -remarks

Prior to Windows Vista and earlier versions of Windows, the <b>RPC_ASYNC_NOTIFICATION_INFO</b> union was part of the <a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure. Please see the <b>RPC_ASYNC_STATE</b> topic for additional information.

## -see-also

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>