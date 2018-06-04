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

# DIRECTMANIPULATION_DRAG_DROP_STATUS enumeration


## -description


Defines the drag-and-drop interaction states for the viewport.


## -enum-fields




### -field DIRECTMANIPULATION_DRAG_DROP_READY

The viewport is at rest and ready for input.


### -field DIRECTMANIPULATION_DRAG_DROP_PRESELECT

The viewport is updating its content and the content is not selected.


### -field DIRECTMANIPULATION_DRAG_DROP_SELECTING

The viewport is updating its content and the content is selected.


### -field DIRECTMANIPULATION_DRAG_DROP_DRAGGING

The viewport is updating its content and the content is being dragged.


### -field DIRECTMANIPULATION_DRAG_DROP_CANCELLED

The viewport has concluded the interaction and requests a revert.


### -field DIRECTMANIPULATION_DRAG_DROP_COMMITTED

The viewport has concluded the interaction and requests a commit.


## -remarks



For each interaction, the status always starts at <b>DIRECTMANIPULATION_DRAG_DROP_READY</b> and ends at either <b>DIRECTMANIPULATION_DRAG_DROP_CANCELLED</b> or <b>DIRECTMANIPULATION_DRAG_DROP_COMMITTED</b>. There are no explicit callbacks for the transition from CANCELLED/COMMITTED to READY.


The meaning of the CANCELLED and COMMITED values depend on the previous status.

<ul>
<li>For <b>DIRECTMANIPULATION_DRAG_DROP_PRESELECT</b>, they mean the same thing: the content goes back to the original location and no other actions should be taken.</li>
<li>FOR <b>DIRECTMANIPULATION_DRAG_DROP_SELECTING</b>, COMMITED means apply the selection change; CANCELLED means avoid the selection change.</li>
<li>For <b>DIRECTMANIPULATION_DRAG_DROP_DRAGGING</b>, COMMITED means perform the drop action; CANCELLED means cancel the drop action.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

