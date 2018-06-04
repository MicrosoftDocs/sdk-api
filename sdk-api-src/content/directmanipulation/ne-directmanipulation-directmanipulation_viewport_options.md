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

# DIRECTMANIPULATION_VIEWPORT_OPTIONS enumeration


## -description


Defines the input behavior options for the viewport.


## -enum-fields




### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_DEFAULT

No special behaviors. This is the default value used to set or revert to default behavior.


### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_AUTODISABLE

At the end of an interaction, the viewport transitions to <a href="https://msdn.microsoft.com/6120702f-56f0-489d-a3b2-5f6ecac82b5e">DIRECTMANIPULATION_READY</a> and then immediately to <b>DIRECTMANIPULATION_DISABLED</b>. The viewport must be explicitly enabled through the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a> method before the next interaction can be processed.


### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE


<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a> must be called to redraw the content within the viewport. The content is not updated automatically during an input event.


### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT

All input from a contact associated with the viewport is passed to the UI thread for processing.


### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_EXPLICITHITTEST

If set, all <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages are passed to the application for hit testing. Otherwise, <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> will process the messages for hit testing against the existing list of running viewports, and the application will not see the input.

Applies only when viewport state is <a href="https://msdn.microsoft.com/6120702f-56f0-489d-a3b2-5f6ecac82b5e">DIRECTMANIPULATION_RUNNING</a> or <b>DIRECTMANIPULATION_INERTIA</b>.


### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_DISABLEPIXELSNAPPING

Specifies that pixel snapping during a manipulation is disabled.

Anti-aliasing can create irregular edge rendering. Artifacts, commonly seen as blurry, or semi-transparent, edges can occur when the location of an edge falls in the middle of a device pixel rather than between device pixels. 


## -remarks



<b>DIRECTMANIPULATION_VIEWPORT_OPTIONS</b> is used in the <a href="https://msdn.microsoft.com/F2B861B9-9E86-4AEE-B86C-03BF37F0988B">SetViewportOptions</a> method. These flags can be combined to set the input behavior for a viewport.




## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

