---
UID: NS:uiautomationcoreapi.UiaStructureChangedEventArgs
title: UiaStructureChangedEventArgs (uiautomationcoreapi.h)
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about an event that is raised when the structure of the Microsoft UI Automation tree changes.
old-location: winauto\uiauto_UiaStructureChangedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 3bd47116-e6e7-4535-a939-460d460a3eb5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UiaStructureChangedEventArgs, UiaStructureChangedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaStructureChangedEventArgsStruct, uiauto_UiaStructureChangedEventArgsStruct, uiautomationcoreapi/UiaStructureChangedEventArgs, winauto.uiauto_UiaStructureChangedEventArgsStruct
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaStructureChangedEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaStructureChangedEventArgs structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about an event that is raised when the structure of the Microsoft UI Automation tree changes.


## -struct-fields




### -field Type

Type: <b><a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a></b>

A value from the <a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a> enumerated type indicating the type of event.


### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -field StructureChangeType

Type: <b><a href="https://msdn.microsoft.com/abaf9551-40c4-4ab6-adb7-b619f3bc9745">StructureChangeType</a></b>

A value from the <a href="https://msdn.microsoft.com/abaf9551-40c4-4ab6-adb7-b619f3bc9745">StructureChangeType</a> enumerated type indicating the type of change that has taken place.


### -field pRuntimeId

Type: <b>int*</b>

The address of an array of runtime identifiers for elements involved in the change.


### -field cRuntimeIdLen

Type: <b>int</b>

The count of elements in the array.

