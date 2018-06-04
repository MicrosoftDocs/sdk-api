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

# InkSystemGesture enumeration


## -description



          Specifies the interest in a set of operating system-specific gestures.


## -enum-fields




### -field ISG_Tap

A click of the left mouse button. This can be used to choose a command from the menu or toolbar, take action if a command is chosen, set an insertion point (IP), or show selection feedback.


### -field ISG_DoubleTap

A double-click of the left mouse button. This can be used to select a word or open a file or folder.


### -field ISG_RightTap

A click of the right mouse button. This can be used to show a shortcut menu.


### -field ISG_Drag

A drag of the mouse while pressing the left mouse button. This can be used to drag-select (such as in Microsoft Word when starting with an IP), select multiple words, drag (such as when dragging an object in Microsoft Windows), or scroll.


### -field ISG_RightDrag

A press and hold followed by a stroke, which maps to a right drag of a mouse. This can be used to drag (such as when dragging an object or selection followed by a shortcut menu).


### -field ISG_HoldEnter

A press and hold of the left mouse button that lasts for a long time, which has no mouse equivalent. This is a fallback for when a user continues a press-and-hold action for a long time and the event reverts to a Tap.


### -field ISG_HoldLeave

Not implemented.


### -field ISG_HoverEnter

A pause of the mouse on an object. This can be used to show a ToolTip, roll-over effects, or other mouse pausing behaviors.


### -field ISG_HoverLeave

A mouse leaving a pause. This can be used to end ToolTip roll-over effects or other mouse pausing behaviors.


### -field ISG_Flick

A flick gesture.


## -remarks



The flick gesture is recognized in Windows Vista and later versions of Windows.

The Windows Vista and Tablet PC operating systems support these gestures by default. When any of these gestures are recognized, the <a href="https://msdn.microsoft.com/11071d6f-8aa3-4902-94fd-89ad0cf17729">SystemGesture</a> event fires automatically. Many of these gestures map to traditional mouse events. For instance, the Tap system gesture mimics a click of the left mouse button.

A system gesture is separate from an application gesture. Application gestures are defined in the <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">InkApplicationGesture</a> enumeration type.

For more information about system gestures, see <a href="https://msdn.microsoft.com/5bc80086-7acf-4f86-a9fb-a663de489f8b">Using Gestures</a>.




## -see-also




<a href="https://msdn.microsoft.com/6c047cf7-2162-4146-906b-47c4006daeeb">GetHotPoint Method</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>



<a href="https://msdn.microsoft.com/36e2ac5a-dc91-47c2-a8e5-e555437c0a5d">SystemGesture Event [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/5bc80086-7acf-4f86-a9fb-a663de489f8b">Using Gestures</a>
 

 

