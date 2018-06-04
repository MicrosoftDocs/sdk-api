---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> containing the old value of the property.


### -field NewValue

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> containing the new value of the property.


## -remarks




    The old value might not be set if the UI Automation provider cannot do so efficiently.
	



