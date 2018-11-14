---
UID: NS:uiautomationcoreapi.UiaPropertyChangedEventArgs
title: UiaPropertyChangedEventArgs
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about an event that is raised when a Microsoft UI Automation element property change occurs.
old-location: winauto\uiauto_UiaPropertyChangedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: d401b971-441e-4a09-9b9a-6725a00154cb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: UiaPropertyChangedEventArgs, UiaPropertyChangedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaPropertyChangedEventArgsStruct, uiauto_UiaPropertyChangedEventArgsStruct, uiautomationcoreapi/UiaPropertyChangedEventArgs, winauto.uiauto_UiaPropertyChangedEventArgsStruct
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - UiaPropertyChangedEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaPropertyChangedEventArgs structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about an event that is raised when a Microsoft UI Automation element property change occurs.


## -struct-fields




### -field Type

Type: <b><a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a></b>

A value from the <a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a> enumerated type indicating the type of event.


### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -field PropertyId

Type: <b>PROPERTYID</b>

The identifier of the property that has changed. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -field OldValue

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a></b>

A <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a> containing the old value of the property.


### -field NewValue

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a></b>

A <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a> containing the new value of the property.


## -remarks



The old value might not be set if the UI Automation provider cannot do so efficiently.
	



