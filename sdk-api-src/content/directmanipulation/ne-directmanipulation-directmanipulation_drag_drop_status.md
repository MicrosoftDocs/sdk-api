---
UID: NE:directmanipulation.DIRECTMANIPULATION_DRAG_DROP_STATUS
title: DIRECTMANIPULATION_DRAG_DROP_STATUS
author: windows-driver-content
description: Defines the drag-and-drop interaction states for the viewport.
old-location: directmanipulation\directmanipulation_drag_drop_status.htm
old-project: directmanipulation
ms.assetid: BC3B8541-E18B-4654-80C8-C5EC1359BE2F
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: DIRECTMANIPULATION_DRAG_DROP_CANCELLED, DIRECTMANIPULATION_DRAG_DROP_COMMITTED, DIRECTMANIPULATION_DRAG_DROP_DRAGGING, DIRECTMANIPULATION_DRAG_DROP_PRESELECT, DIRECTMANIPULATION_DRAG_DROP_READY, DIRECTMANIPULATION_DRAG_DROP_SELECTING, DIRECTMANIPULATION_DRAG_DROP_STATUS, DIRECTMANIPULATION_DRAG_DROP_STATUS enumeration [Direct Manipulation], directmanipulation.directmanipulation_drag_drop_status, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_CANCELLED, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_COMMITTED, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_DRAGGING, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_PRESELECT, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_READY, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_SELECTING, directmanipulation/DIRECTMANIPULATION_DRAG_DROP_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DIRECTMANIPULATION_DRAG_DROP_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	directmanipulation.h
api_name:
-	DIRECTMANIPULATION_DRAG_DROP_STATUS
product: Windows
targetos: Windows
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
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
 

 

