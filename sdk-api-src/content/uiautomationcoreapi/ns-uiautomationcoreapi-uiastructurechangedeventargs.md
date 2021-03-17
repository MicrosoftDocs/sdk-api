---
UID: NS:uiautomationcoreapi.UiaStructureChangedEventArgs
title: UiaStructureChangedEventArgs (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about an event that is raised when the structure of the Microsoft UI Automation tree changes.
helpviewer_keywords: ["UiaStructureChangedEventArgs","UiaStructureChangedEventArgs structure [Windows Accessibility]","uiauto.uiauto_UiaStructureChangedEventArgsStruct","uiauto_UiaStructureChangedEventArgsStruct","uiautomationcoreapi/UiaStructureChangedEventArgs","winauto.uiauto_UiaStructureChangedEventArgsStruct"]
old-location: winauto\uiauto_UiaStructureChangedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 3bd47116-e6e7-4535-a939-460d460a3eb5
ms.date: 12/05/2018
ms.keywords: UiaStructureChangedEventArgs, UiaStructureChangedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaStructureChangedEventArgsStruct, uiauto_UiaStructureChangedEventArgsStruct, uiautomationcoreapi/UiaStructureChangedEventArgs, winauto.uiauto_UiaStructureChangedEventArgsStruct
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
 - UiaStructureChangedEventArgs
 - uiautomationcoreapi/UiaStructureChangedEventArgs
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
 - UiaStructureChangedEventArgs
---

# UiaStructureChangedEventArgs structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about an event that is raised when the structure of the Microsoft UI Automation tree changes.

## -struct-fields

### -field Type

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a> enumerated type indicating the type of event.

### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -field StructureChangeType

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType</a> enumerated type indicating the type of change that has taken place.

### -field pRuntimeId

Type: <b>int*</b>

The address of an array of runtime identifiers for elements involved in the change.

### -field cRuntimeIdLen

Type: <b>int</b>

The count of elements in the array.