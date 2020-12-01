---
UID: NE:uiautomationcoreapi.EventArgsType
title: EventArgsType (uiautomationcoreapi.h)
description: Contains values that specify the event type described by a UiaEventArgs structure.
helpviewer_keywords: ["EventArgsType","EventArgsType enumeration [Windows Accessibility]","EventArgsType_AsyncContentLoaded","EventArgsType_Changes","EventArgsType_Notification","EventArgsType_PropertyChanged","EventArgsType_Simple","EventArgsType_StructureChanged","EventArgsType_TextEditTextChanged","EventArgsType_WindowClosed","uiauto.uiauto_EventArgsTypeEnum","uiauto_EventArgsTypeEnum","uiautomationcoreapi/EventArgsType","uiautomationcoreapi/EventArgsType_AsyncContentLoaded","uiautomationcoreapi/EventArgsType_Changes","uiautomationcoreapi/EventArgsType_Notification","uiautomationcoreapi/EventArgsType_PropertyChanged","uiautomationcoreapi/EventArgsType_Simple","uiautomationcoreapi/EventArgsType_StructureChanged","uiautomationcoreapi/EventArgsType_TextEditTextChanged","uiautomationcoreapi/EventArgsType_WindowClosed","winauto.uiauto_EventArgsTypeEnum"]
old-location: winauto\uiauto_EventArgsTypeEnum.htm
tech.root: WinAuto
ms.assetid: b62712cc-bb00-44b0-9664-cc8edbfabb0a
ms.date: 09/24/2020
ms.keywords: EventArgsType, EventArgsType enumeration [Windows Accessibility], EventArgsType_AsyncContentLoaded, EventArgsType_Changes, EventArgsType_Notification, EventArgsType_PropertyChanged, EventArgsType_Simple, EventArgsType_StructureChanged, EventArgsType_TextEditTextChanged, EventArgsType_WindowClosed, uiauto.uiauto_EventArgsTypeEnum, uiauto_EventArgsTypeEnum, uiautomationcoreapi/EventArgsType, uiautomationcoreapi/EventArgsType_AsyncContentLoaded, uiautomationcoreapi/EventArgsType_Changes, uiautomationcoreapi/EventArgsType_Notification, uiautomationcoreapi/EventArgsType_PropertyChanged, uiautomationcoreapi/EventArgsType_Simple, uiautomationcoreapi/EventArgsType_StructureChanged, uiautomationcoreapi/EventArgsType_TextEditTextChanged, uiautomationcoreapi/EventArgsType_WindowClosed, winauto.uiauto_EventArgsTypeEnum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventArgsType
 - uiautomationcoreapi/EventArgsType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - EventArgsType
---

# EventArgsType enumeration


## -description

Contains values that specify the event type described by a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiaeventargs">UiaEventArgs</a> structure.

## -enum-fields

### -field EventArgsType_Simple

A simple event that does not provide data in the event arguments.

### -field EventArgsType_PropertyChanged

An event raised by calling the [UiaRaiseAutomationPropertyChangedEvent function](nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent.md).

### -field EventArgsType_StructureChanged

An event raised by calling the [UiaRaiseStructureChangedEvent function](nf-uiautomationcoreapi-uiaraisestructurechangedevent.md).

### -field EventArgsType_AsyncContentLoaded

An event raised by calling the [UiaRaiseAsyncContentLoadedEvent function](nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent.md).

### -field EventArgsType_WindowClosed

An event raised when a window is closed.

### -field EventArgsType_TextEditTextChanged

An event raised by calling the [UiaRaiseTextEditTextChangedEvent function](nf-uiautomationcoreapi-uiaraisetextedittextchangedevent.md)

### -field EventArgsType_Changes

An event raised by calling the [UiaRaiseChangesEvent function](nf-uiautomationcoreapi-uiaraisechangesevent.md).

### -field EventArgsType_Notification

An event raised by calling the [UiaRaiseNotificationEvent function](nf-uiautomationcoreapi-uiaraisenotificationevent.md).

### -field EventArgsType_ActiveTextPositionChanged

An event raised by calling the [UiaRaiseActiveTextPositionChangedEvent function](nf-uiautomationcoreapi-uiaraiseactivetextpositionchangedevent.md).
