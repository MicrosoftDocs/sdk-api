---
UID: NE:prnasnot.PrintAsyncNotifyError
title: PrintAsyncNotifyError
author: windows-sdk-content
description: Specifies the error code portion of the HRESULT returned after an asynchronous notification failure.
old-location: gdi\printasyncnotifyerror.htm
old-project: printdocs
ms.assetid: 2fb6698c-5d59-4ba0-a8ff-1313fade438c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ALREADY_REGISTERED, ALREADY_UNREGISTERED, ASYNC_CALL_ALREADY_PARKED, ASYNC_CALL_IN_PROGRESS, ASYNC_NOTIFICATION_FAILURE, CHANNEL_ACQUIRED, CHANNEL_ALREADY_CLOSED, CHANNEL_ALREADY_OPENED, CHANNEL_CLOSED_BY_ANOTHER_LISTENER, CHANNEL_CLOSED_BY_SAME_LISTENER, CHANNEL_CLOSED_BY_SERVER, CHANNEL_NOT_OPENED, CHANNEL_RELEASED_BY_LISTENER, CHANNEL_WAITING_FOR_CLIENT_NOTIFICATION, INTERNAL_NOTIFICATION_QUEUE_IS_FULL, INVALID_NOTIFICATION_TYPE, LOCAL_ONLY_REGISTRATION, MAX_CHANNEL_COUNT_EXCEEDED, MAX_NOTIFICATION_SIZE_EXCEEDED, MAX_REGISTRATION_COUNT_EXCEEDED, NOT_REGISTERED, NO_LISTENERS, PrintAsyncNotifyError, PrintAsyncNotifyError enumeration [Windows GDI], REMOTE_ONLY_REGISTRATION, UNIRECTIONAL_NOTIFICATION_LOST, _win32_PrintAsyncNotifyError, gdi.printasyncnotifyerror, prnasnot/ALREADY_REGISTERED, prnasnot/ALREADY_UNREGISTERED, prnasnot/ASYNC_CALL_ALREADY_PARKED, prnasnot/ASYNC_CALL_IN_PROGRESS, prnasnot/ASYNC_NOTIFICATION_FAILURE, prnasnot/CHANNEL_ACQUIRED, prnasnot/CHANNEL_ALREADY_CLOSED, prnasnot/CHANNEL_ALREADY_OPENED, prnasnot/CHANNEL_CLOSED_BY_ANOTHER_LISTENER, prnasnot/CHANNEL_CLOSED_BY_SAME_LISTENER, prnasnot/CHANNEL_CLOSED_BY_SERVER, prnasnot/CHANNEL_NOT_OPENED, prnasnot/CHANNEL_RELEASED_BY_LISTENER, prnasnot/CHANNEL_WAITING_FOR_CLIENT_NOTIFICATION, prnasnot/INTERNAL_NOTIFICATION_QUEUE_IS_FULL, prnasnot/INVALID_NOTIFICATION_TYPE, prnasnot/LOCAL_ONLY_REGISTRATION, prnasnot/MAX_CHANNEL_COUNT_EXCEEDED, prnasnot/MAX_NOTIFICATION_SIZE_EXCEEDED, prnasnot/MAX_REGISTRATION_COUNT_EXCEEDED, prnasnot/NOT_REGISTERED, prnasnot/NO_LISTENERS, prnasnot/PrintAsyncNotifyError, prnasnot/REMOTE_ONLY_REGISTRATION, prnasnot/UNIRECTIONAL_NOTIFICATION_LOST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: prnasnot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Printmanagerinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PrintAsyncNotifyError
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - prnasnot.h
api_name:
 - PrintAsyncNotifyError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PrintAsyncNotifyError enumeration


## -description


Specifies the error code portion of the <b>HRESULT</b> returned after an asynchronous notification failure.

An <b>HRESULT</b> value consists of a severity code, a facility code, and an error code. Use the <b>HRESULT_CODE</b> macro to compare just the error code of an <b>HRESULT</b>. For more information about COM error codes, see 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.


## -enum-fields




### -field CHANNEL_CLOSED_BY_SERVER

The Print Spooler-hosted printing system component closed the communication channel.


### -field CHANNEL_CLOSED_BY_ANOTHER_LISTENER

A listening application, other than the caller, closed the communication channel.


### -field CHANNEL_CLOSED_BY_SAME_LISTENER

The caller has already closed the communication channel.


### -field CHANNEL_RELEASED_BY_LISTENER

The caller has already released the communication channel


### -field UNIRECTIONAL_NOTIFICATION_LOST

One or more listeners did not receive this notification however; at least one listener did receive this notification.


### -field ASYNC_NOTIFICATION_FAILURE

There was a problem sending this notification. None of the listeners on this channel are configured to receive this notification type or there was a problem allocating the resources necessary to complete this call.


### -field NO_LISTENERS

Indicates that there are no registered listening applications.


### -field CHANNEL_ALREADY_CLOSED

The channel has already been closed.


### -field CHANNEL_ALREADY_OPENED

The channel has already been opened.


### -field CHANNEL_WAITING_FOR_CLIENT_NOTIFICATION

A notification cannot be sent because a response to the last notification has not been received.


### -field CHANNEL_NOT_OPENED

The channel is not yet open.


### -field ASYNC_CALL_ALREADY_PARKED

A notification cannot be sent because the recipient has not consumed the previous notification.


### -field NOT_REGISTERED

The listening application is not registered for notifications of the specified type from the specified queue or print server.


### -field ALREADY_UNREGISTERED

The listening application has already unregistered.


### -field ALREADY_REGISTERED

The listening application has already registered for notifications of the specified type from the specified queue or print server.


### -field CHANNEL_ACQUIRED

Another listener on this channel has already responded. Only the first respondent can continue the communication with the sender.


### -field ASYNC_CALL_IN_PROGRESS

The channel is busy with another notification or response.


### -field MAX_NOTIFICATION_SIZE_EXCEEDED

The maximum size of the notification data has been exceeded. By default, the maximum data size allowed is 10 Megabytes.


### -field INTERNAL_NOTIFICATION_QUEUE_IS_FULL

The Print Spooler cannot hold any more queued notifications. By default, a maximum number of 10 notifications are allowed to be queued.


### -field INVALID_NOTIFICATION_TYPE

The specified notification type is invalid.


### -field MAX_REGISTRATION_COUNT_EXCEEDED

No more applications can register for this type of notification on the specified queue or print server. The maximum number of such registrations is 10,000 by default.


### -field MAX_CHANNEL_COUNT_EXCEEDED

The print spooler has already created the maximum number of channels and cannot create any more. The maximum number of channels the print spooler can create is 10,000 by default.


### -field LOCAL_ONLY_REGISTRATION

Registration for local notification was successful. Registration for remote notification was not.


### -field REMOTE_ONLY_REGISTRATION

Registration for remote notification was successful. Registration for local notification was not.

