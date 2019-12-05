---
UID: NE:uiautomationcore.NotificationKind
title: NotificationKind (uiautomationcore.h)
description: Defines values that indicate the type of a notification event, and a hint to the listener about the processing of the event.
old-location: winauto\uiauto_NotificationKind.htm
tech.root: WinAuto
ms.assetid: A74C1897-F762-4D7B-9A4D-6D09B9564A7C
ms.date: 12/05/2018
ms.keywords: NotificationKind, NotificationKind enumeration [Windows Accessibility], NotificationKind_ActionAborted, NotificationKind_ActionCompleted, NotificationKind_ItemAdded, NotificationKind_ItemRemoved, NotificationKind_Other, uiautomationclient/ NotificationKind_ActionCompleted, uiautomationclient/ NotificationKind_ItemAdded, uiautomationclient/ NotificationKind_ItemRemoved, uiautomationclient/NotificationKind, uiautomationclient/NotificationKind_ActionAborted, uiautomationclient/NotificationKind_Other, winauto.uiauto_NotificationKind
ms.topic: enum
f1_keywords:
- uiautomationcore/NotificationKind
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
- NotificationKind
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NotificationKind enumeration


## -description


Defines values that indicate the type of a notification event, and a hint to the listener about the processing of the event. For example, if multiple notifications are received, they should all be read, or only the last one should be read, and so on.


## -enum-fields




### -field NotificationKind_ItemAdded

The current element and/or the container has had something added to it that should be presented to the user.


### -field NotificationKind_ItemRemoved

The current element has had something removed from inside of it that should be presented to the user.


### -field NotificationKind_ActionCompleted

The current element has a notification that an action was completed.


### -field NotificationKind_ActionAborted

The current element has a notification that an action was aborted.


### -field NotificationKind_Other

The current element has a notification not an add, remove, completed, or aborted action.

