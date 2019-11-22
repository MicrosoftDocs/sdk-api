---
UID: NE:uiautomationcore.NotificationProcessing
title: NotificationProcessing (uiautomationcore.h)

description: Defines values that indicate how a notification should be processed.
old-location: winauto\uiauto_NotificationProcessing.htm
tech.root: WinAuto
ms.assetid: 5A6969E1-2350-4418-B02A-0C92D8A246A1

ms.date: 12/05/2018
ms.keywords: NotificationProcessing, NotificationProcessing enumeration [Windows Accessibility], NotificationProcessing_All, NotificationProcessing_CurrentThenMostRecent, NotificationProcessing_ImportantAll, NotificationProcessing_ImportantMostRecent, NotificationProcessing_MostRecent, uiautomationclient/NotificationProcessing, uiautomationclient/NotificationProcessing_All, uiautomationclient/NotificationProcessing_CurrentThenMostRecent, uiautomationclient/NotificationProcessing_ImportantAll, uiautomationclient/NotificationProcessing_ImportantMostRecent, uiautomationclient/NotificationProcessing_MostRecent, winauto.uiauto_NotificationProcessing
ms.topic: enum
f1_keywords: 
 - "uiautomationcore/NotificationProcessing"
dev_langs:
 - c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h, Uiautomationcore.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - NotificationProcessing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NotificationProcessing enumeration


## -description


Defines values that indicate how a notification should be processed.


## -enum-fields




### -field NotificationProcessing_ImportantAll

These notifications should be presented to the user as soon as possible and 
all of the notifications from this source should be delivered to the user.

<div class="alert"><b>Warning</b>  Use this in a limited capacity as this style of message could cause a flooding of information to the user due to the nature of the request to deliver all notifications.</div>
<div> </div>

### -field NotificationProcessing_ImportantMostRecent

These notifications 
should be presented to the user as soon as possible. The most recent notification from this source should be delivered to the user because it supersedes all of the other notifications.


### -field NotificationProcessing_All

These notifications 
should be presented to the user when possible. 
All of the notifications from this source should be delivered to the user.


### -field NotificationProcessing_MostRecent

These notifications 
should be presented to the user when possible. The most recent notification from this source should be delivered to the user because it supersedes all of the other notifications.


### -field NotificationProcessing_CurrentThenMostRecent

These notifications 
should be presented to the user when possible. 
Don’t interrupt the current notification for this one.
If new notifications come in from the same source while the current notification is being presented, keep the most recent and ignore the rest until the current processing is completed.  Then, use the most recent message as the current message.

