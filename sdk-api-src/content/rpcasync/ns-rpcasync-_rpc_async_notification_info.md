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

# _RPC_ASYNC_NOTIFICATION_INFO structure


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
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


### -field IOC.dwCompletionKey

Set by the RPC client before the asynchronous call is started. When the notification is delivered to the completion port, this value is filled in the location pointed to by the <i>lpCompletionKey</i> parameter of the 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


### -field IOC.lpOverlapped

Set by the RPC client before the asynchronous call is started. When the notification is delivered to the completion port, this value is filled in the location pointed to by the <i>lpOverlapped</i> parameter of the 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


### -field HWND

Fields used for notification by a Windows message. When the RPC run time posts the message, <b>wParam</b> is zero, and <b>lParam</b> points to the asynchronous handle for the call (the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>).

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

Windows 7 or later versions of Windows: An optional function pointer to a user-defined notification scheme built on top of RPC call completion. As an example, an application could call <a href="https://msdn.microsoft.com/28df173d-b78c-4158-97d5-63117a2d3967">SubmitThreadpoolWork</a> from the notification callback.

<div class="alert"><b>Note</b>  Making additional RPC calls, blocking,  or performing long running work from notification callbacks is strongly discouraged.</div>
<div> </div>

## -remarks



Prior to Windows Vista and earlier versions of Windows, the <b>RPC_ASYNC_NOTIFICATION_INFO</b> union was part of the <a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure. Please see the <b>RPC_ASYNC_STATE</b> topic for additional information.




## -see-also




<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>
 

 

