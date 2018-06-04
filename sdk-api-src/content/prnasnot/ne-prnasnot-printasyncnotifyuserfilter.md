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

# PrintAsyncNotifyUserFilter enumeration


## -description


Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.


## -enum-fields




### -field kPerUser

When passed to <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel
</a>, kPerUser indicates that notifications will go only to listening applications that are using <a href="https://msdn.microsoft.com/a3f74372-bdc9-43eb-b72f-7d00a43e78a8">Client Impersonation</a> to impersonate the same user as the Print Spooler-hosted sender. For example, if the Print Spooler-hosted sender sends a notification that a print job has finished printing, only listening applications impersonating the user that submitted the job will receive notification. When passed to <a href="https://msdn.microsoft.com/f5a01819-75d0-42a0-b66f-5a25a48b091c">RegisterForPrintAsyncNotifications</a>, kPerUser indicates that the listener will receive notifications only from senders that are impersonating the same user as the listener.


### -field kAllUsers

When passed to <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel
</a>, kAllUsers indicates that notifications will go to all listening applications, regardless of the user; as long as the sender has administration privileges on the associated print queue or print server. When passed to <a href="https://msdn.microsoft.com/f5a01819-75d0-42a0-b66f-5a25a48b091c">RegisterForPrintAsyncNotifications</a>, kAllUsers indicates that notifications will go to all listening applications whose associated user has administration privileges on the print queue or print server.


## -remarks



Regardless of which value is passed, listeners will receive only the types of notifications for which they have registered.

A user may be simultaneously logged on to multiple terminal server sessions. All of the user's applications, regardless of which session hosts them, will receive notifications for which they have registered.



