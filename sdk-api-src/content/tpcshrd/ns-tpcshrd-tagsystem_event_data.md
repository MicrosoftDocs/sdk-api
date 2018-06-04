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

# tagSYSTEM_EVENT_DATA structure


## -description



Contains information about a tablet system event.




## -struct-fields




### -field bModifier

Bit values for the modifiers. Possible values include SE_MODIFIER_CTRL (the Control key was pressed), SE_MODIFIER_ALT (the Alt key was pressed), and SE_MODIFIER_SHIFT (the Shift key was pressed).


### -field wKey

Scan code for the keyboard character.


### -field xPos

X position of the event.


### -field yPos

Y position of the event.


### -field bCursorMode

The type of cursor that caused the event. Possible values include SE_NORMAL_CURSOR (the pen tip) and SE_ERASER_CURSOR (the eraser).


### -field dwButtonState

State of the buttons at the time of the system event.


## -see-also




<a href="https://msdn.microsoft.com/7cdba29e-0599-45f7-8853-3e8fa29897e8">IStylusPlugin::SystemEvent Method</a>



<a href="https://msdn.microsoft.com/3d9e98f0-b11e-4a65-a544-9e1998a80d5f">ITabletEventSink::SystemEvent Method</a>
 

 

