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

