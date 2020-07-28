---
UID: NE:uiautomationcoreapi.EventArgsType
title: EventArgsType (uiautomationcoreapi.h)
description: Contains values that specify the event type described by a UiaEventArgs structure.
helpviewer_keywords: ["EventArgsType","EventArgsType enumeration [Windows Accessibility]","EventArgsType_AsyncContentLoaded","EventArgsType_Changes","EventArgsType_Notification","EventArgsType_PropertyChanged","EventArgsType_Simple","EventArgsType_StructureChanged","EventArgsType_TextEditTextChanged","EventArgsType_WindowClosed","uiauto.uiauto_EventArgsTypeEnum","uiauto_EventArgsTypeEnum","uiautomationcoreapi/EventArgsType","uiautomationcoreapi/EventArgsType_AsyncContentLoaded","uiautomationcoreapi/EventArgsType_Changes","uiautomationcoreapi/EventArgsType_Notification","uiautomationcoreapi/EventArgsType_PropertyChanged","uiautomationcoreapi/EventArgsType_Simple","uiautomationcoreapi/EventArgsType_StructureChanged","uiautomationcoreapi/EventArgsType_TextEditTextChanged","uiautomationcoreapi/EventArgsType_WindowClosed","winauto.uiauto_EventArgsTypeEnum"]
old-location: winauto\uiauto_EventArgsTypeEnum.htm
tech.root: WinAuto
ms.assetid: b62712cc-bb00-44b0-9664-cc8edbfabb0a
ms.date: 12/05/2018
ms.keywords: EventArgsType, EventArgsType enumeration [Windows Accessibility], EventArgsType_AsyncContentLoaded, EventArgsType_Changes, EventArgsType_Notification, EventArgsType_PropertyChanged, EventArgsType_Simple, EventArgsType_StructureChanged, EventArgsType_TextEditTextChanged, EventArgsType_WindowClosed, uiauto.uiauto_EventArgsTypeEnum, uiauto_EventArgsTypeEnum, uiautomationcoreapi/EventArgsType, uiautomationcoreapi/EventArgsType_AsyncContentLoaded, uiautomationcoreapi/EventArgsType_Changes, uiautomationcoreapi/EventArgsType_Notification, uiautomationcoreapi/EventArgsType_PropertyChanged, uiautomationcoreapi/EventArgsType_Simple, uiautomationcoreapi/EventArgsType_StructureChanged, uiautomationcoreapi/EventArgsType_TextEditTextChanged, uiautomationcoreapi/EventArgsType_WindowClosed, winauto.uiauto_EventArgsTypeEnum
f1_keywords:
- uiautomationcoreapi/EventArgsType
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- UIAutomationCoreApi.h
api_name:
- EventArgsType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventArgsType enumeration


## -description


Contains values that specify the event type described by a <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiaeventargs">UiaEventArgs</a> structure.


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

An event raised by calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisechangesevent">UiaRaiseChangesEvent</a>.


### -field EventArgsType_Notification

An event raised by calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisenotificationevent">UiaRaiseNotificationEvent</a>.


### -field EventArgsType_ActiveTextPositionChanged



