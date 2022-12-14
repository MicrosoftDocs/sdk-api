---
UID: NE:uiautomationcore.NotificationProcessing
title: NotificationProcessing (uiautomationcore.h)
description: Defines values that indicate how a notification should be processed.
helpviewer_keywords: ["NotificationProcessing","NotificationProcessing enumeration [Windows Accessibility]","NotificationProcessing_All","NotificationProcessing_CurrentThenMostRecent","NotificationProcessing_ImportantAll","NotificationProcessing_ImportantMostRecent","NotificationProcessing_MostRecent","uiautomationclient/NotificationProcessing","uiautomationclient/NotificationProcessing_All","uiautomationclient/NotificationProcessing_CurrentThenMostRecent","uiautomationclient/NotificationProcessing_ImportantAll","uiautomationclient/NotificationProcessing_ImportantMostRecent","uiautomationclient/NotificationProcessing_MostRecent","winauto.uiauto_NotificationProcessing"]
old-location: winauto\uiauto_NotificationProcessing.htm
tech.root: WinAuto
ms.assetid: 5A6969E1-2350-4418-B02A-0C92D8A246A1
ms.date: 12/05/2018
ms.keywords: NotificationProcessing, NotificationProcessing enumeration [Windows Accessibility], NotificationProcessing_All, NotificationProcessing_CurrentThenMostRecent, NotificationProcessing_ImportantAll, NotificationProcessing_ImportantMostRecent, NotificationProcessing_MostRecent, uiautomationclient/NotificationProcessing, uiautomationclient/NotificationProcessing_All, uiautomationclient/NotificationProcessing_CurrentThenMostRecent, uiautomationclient/NotificationProcessing_ImportantAll, uiautomationclient/NotificationProcessing_ImportantMostRecent, uiautomationclient/NotificationProcessing_MostRecent, winauto.uiauto_NotificationProcessing
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NotificationProcessing
 - uiautomationcore/NotificationProcessing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - NotificationProcessing
---

# NotificationProcessing enumeration


## -description

Defines values that indicate how a notification should be processed.

## -enum-fields

### -field NotificationProcessing_ImportantAll:0

These notifications should be presented to the user as soon as possible and 
all of the notifications from this source should be delivered to the user.

<div class="alert"><b>Warning</b>  Use this in a limited capacity as this style of message could cause a flooding of information to the user due to the nature of the request to deliver all notifications.</div>
<div> </div>

### -field NotificationProcessing_ImportantMostRecent:1

These notifications 
should be presented to the user as soon as possible. The most recent notification from this source should be delivered to the user because it supersedes all of the other notifications.

### -field NotificationProcessing_All:2

These notifications 
should be presented to the user when possible. 
All of the notifications from this source should be delivered to the user.

### -field NotificationProcessing_MostRecent:3

These notifications 
should be presented to the user when possible. The most recent notification from this source should be delivered to the user because it supersedes all of the other notifications.

### -field NotificationProcessing_CurrentThenMostRecent:4

These notifications 
should be presented to the user when possible. 
Don’t interrupt the current notification for this one.
If new notifications come in from the same source while the current notification is being presented, keep the most recent and ignore the rest until the current processing is completed.  Then, use the most recent message as the current message.

