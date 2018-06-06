---
UID: NS:tpcshrd.tagSYSTEM_EVENT_DATA
title: tagSYSTEM_EVENT_DATA
author: windows-sdk-content
description: Contains information about a tablet system event.
old-location: tablet\system_event_data.htm
old-project: tablet
ms.assetid: 3a2c33b7-91ca-48eb-a5b9-a1ccb5106f90
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 3a2c33b7-91ca-48eb-a5b9-a1ccb5106f90, SYSTEM_EVENT_DATA, SYSTEM_EVENT_DATA structure [Tablet PC], tablet.system_event_data, tagSYSTEM_EVENT_DATA, tpcshrd/SYSTEM_EVENT_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tpcshrd.h
req.include-header: RTSCom.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYSTEM_EVENT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - SYSTEM_EVENT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

