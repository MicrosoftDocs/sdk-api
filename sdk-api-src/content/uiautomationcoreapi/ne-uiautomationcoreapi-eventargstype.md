---
UID: NE:uiautomationcoreapi.EventArgsType
title: EventArgsType
author: windows-driver-content
description: Contains values that specify the event type described by a UiaEventArgs structure.
old-location: winauto\uiauto_EventArgsTypeEnum.htm
old-project: WinAuto
ms.assetid: b62712cc-bb00-44b0-9664-cc8edbfabb0a
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: EventArgsType, EventArgsType enumeration [Windows Accessibility], EventArgsType_AsyncContentLoaded, EventArgsType_Changes, EventArgsType_Notification, EventArgsType_PropertyChanged, EventArgsType_Simple, EventArgsType_StructureChanged, EventArgsType_TextEditTextChanged, EventArgsType_WindowClosed, uiauto.uiauto_EventArgsTypeEnum, uiauto_EventArgsTypeEnum, uiautomationcoreapi/EventArgsType, uiautomationcoreapi/EventArgsType_AsyncContentLoaded, uiautomationcoreapi/EventArgsType_Changes, uiautomationcoreapi/EventArgsType_Notification, uiautomationcoreapi/EventArgsType_PropertyChanged, uiautomationcoreapi/EventArgsType_Simple, uiautomationcoreapi/EventArgsType_StructureChanged, uiautomationcoreapi/EventArgsType_TextEditTextChanged, uiautomationcoreapi/EventArgsType_WindowClosed, winauto.uiauto_EventArgsTypeEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAutomationCoreApi.h
api_name:
-	EventArgsType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# EventArgsType enumeration


## -description


Contains values that specify the event type described by a <a href="https://msdn.microsoft.com/7598936c-85da-40bc-8e94-94543371d915">UiaEventArgs</a> structure.


## -enum-fields




### -field EventArgsType_Simple

A simple event that does not provide data in the event arguments.


### -field EventArgsType_PropertyChanged

An event raised by a property change.


### -field EventArgsType_StructureChanged

An event raised by a change in the UI Automation tree structure.


### -field EventArgsType_AsyncContentLoaded

An event raised during asynchronous loading of content by an element.


### -field EventArgsType_WindowClosed

An event raised when a window is closed.


### -field EventArgsType_TextEditTextChanged

An event raised by a change in editable text.


### -field EventArgsType_Changes

An event raised by calling <a href="https://msdn.microsoft.com/AA6F1F6E-3EE9-44A6-B1AE-B08013DC1E37">UiaRaiseChangesEvent</a>.


### -field EventArgsType_Notification

An event raised by calling <a href="https://msdn.microsoft.com/E9555BC0-A53B-416F-95C3-53696716F61F">UiaRaiseNotificationEvent</a>.

