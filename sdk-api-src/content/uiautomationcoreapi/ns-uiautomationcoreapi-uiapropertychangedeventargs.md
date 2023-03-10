---
UID: NS:uiautomationcoreapi.UiaPropertyChangedEventArgs
title: UiaPropertyChangedEventArgs (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about an event that is raised when a Microsoft UI Automation element property change occurs.
helpviewer_keywords: ["UiaPropertyChangedEventArgs","UiaPropertyChangedEventArgs structure [Windows Accessibility]","uiauto.uiauto_UiaPropertyChangedEventArgsStruct","uiauto_UiaPropertyChangedEventArgsStruct","uiautomationcoreapi/UiaPropertyChangedEventArgs","winauto.uiauto_UiaPropertyChangedEventArgsStruct"]
old-location: winauto\uiauto_UiaPropertyChangedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: d401b971-441e-4a09-9b9a-6725a00154cb
ms.date: 12/05/2018
ms.keywords: UiaPropertyChangedEventArgs, UiaPropertyChangedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaPropertyChangedEventArgsStruct, uiauto_UiaPropertyChangedEventArgsStruct, uiautomationcoreapi/UiaPropertyChangedEventArgs, winauto.uiauto_UiaPropertyChangedEventArgsStruct
req.header: uiautomationcoreapi.h
req.include-header: 
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
 - UiaPropertyChangedEventArgs
 - uiautomationcoreapi/UiaPropertyChangedEventArgs
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
 - UiaPropertyChangedEventArgs
---

# UiaPropertyChangedEventArgs structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about an event that is raised when a Microsoft UI Automation element property change occurs.

## -struct-fields

### -field Type

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a> enumerated type indicating the type of event.

### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -field PropertyId

Type: <b>PROPERTYID</b>

The identifier of the property that has changed. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -field OldValue

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

A <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> containing the old value of the property.

### -field NewValue

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

A <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> containing the new value of the property.

## -remarks

The old value might not be set if the UI Automation provider cannot do so efficiently.