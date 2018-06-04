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

# InkCollectorEventInterest enumeration


## -description



Defines values that are used to specify whether an event occurred on an ink collector and, if so, which event fired. To get the status of a given event, call the <a href="https://msdn.microsoft.com/532a798e-b434-4730-8c20-7ec60255f170">GetEventInterest</a> method. To set the status of a given event, call the <a href="https://msdn.microsoft.com/df25efbb-5229-4211-948f-3a213154a967">SetEventInterest</a> method.




## -enum-fields




### -field ICEI_DefaultEvents

The ink collector is interested in the <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a>, <a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange</a>, and <a href="https://msdn.microsoft.com/a3a570ed-570b-4579-b120-ed5457630bc2">CursorOutOfRange</a> events.


### -field ICEI_CursorDown

The ink collector detects a cursor down.


### -field ICEI_Stroke

Specifies that a new stroke is drawn on a tablet.


### -field ICEI_NewPackets

The ink collector receives a <i>packet</i>.


### -field ICEI_NewInAirPackets

The ink collector detects an in-air packet.


### -field ICEI_CursorButtonDown

The ink collector detects a cursor button down.


### -field ICEI_CursorButtonUp

The ink collector detects a cursor button up.


### -field ICEI_CursorInRange

Specifies that a cursor is detected in range of a tablet.


### -field ICEI_CursorOutOfRange

Specifies that a cursor is detected leaving the range of a tablet.


### -field ICEI_SystemGesture

The ink collector recognizes a system gesture.


### -field ICEI_TabletAdded

Specifies that a tablet was added to the system.


### -field ICEI_TabletRemoved

Specifies that a tablet was removed from the system.


### -field ICEI_MouseDown

The mouse pointer is over the object and a mouse button is pressed.


### -field ICEI_MouseMove

The mouse pointer is moved over the object.


### -field ICEI_MouseUp

The mouse pointer is over the object and a mouse button is released.


### -field ICEI_MouseWheel

The mouse wheel moves while the object has focus.


### -field ICEI_DblClick

The object was double-clicked.


### -field ICEI_AllEvents

The ink collector recognizes all events.


## -see-also




<a href="https://msdn.microsoft.com/532a798e-b434-4730-8c20-7ec60255f170">GetEventInterest Method</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>



<a href="https://msdn.microsoft.com/df25efbb-5229-4211-948f-3a213154a967">SetEventInterest Method</a>
 

 

