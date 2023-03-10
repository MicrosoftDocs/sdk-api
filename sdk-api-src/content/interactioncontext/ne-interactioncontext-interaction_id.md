---
UID: NE:interactioncontext.INTERACTION_ID
title: INTERACTION_ID (interactioncontext.h)
description: Specifies the interaction states used for configuring an Interaction Context object.
helpviewer_keywords: ["INTERACTION_ID","INTERACTION_ID enumeration","INTERACTION_ID_CROSS_SLIDE","INTERACTION_ID_DRAG","INTERACTION_ID_HOLD","INTERACTION_ID_MANIPULATION","INTERACTION_ID_MAX","INTERACTION_ID_NONE","INTERACTION_ID_SECONDARY_TAP","INTERACTION_ID_TAP","input_intcontext.interaction_id","interactioncontext.interaction_id","interactioncontext/INTERACTION_ID","interactioncontext/INTERACTION_ID_CROSS_SLIDE","interactioncontext/INTERACTION_ID_DRAG","interactioncontext/INTERACTION_ID_HOLD","interactioncontext/INTERACTION_ID_MANIPULATION","interactioncontext/INTERACTION_ID_MAX","interactioncontext/INTERACTION_ID_NONE","interactioncontext/INTERACTION_ID_SECONDARY_TAP","interactioncontext/INTERACTION_ID_TAP"]
old-location: input_intcontext\interaction_id.htm
tech.root: input_intcontext
ms.assetid: 9c6ac9ce-d7c9-4a92-9631-2f241a762525
ms.date: 12/05/2018
ms.keywords: INTERACTION_ID, INTERACTION_ID enumeration, INTERACTION_ID_CROSS_SLIDE, INTERACTION_ID_DRAG, INTERACTION_ID_HOLD, INTERACTION_ID_MANIPULATION, INTERACTION_ID_MAX, INTERACTION_ID_NONE, INTERACTION_ID_SECONDARY_TAP, INTERACTION_ID_TAP, input_intcontext.interaction_id, interactioncontext.interaction_id, interactioncontext/INTERACTION_ID, interactioncontext/INTERACTION_ID_CROSS_SLIDE, interactioncontext/INTERACTION_ID_DRAG, interactioncontext/INTERACTION_ID_HOLD, interactioncontext/INTERACTION_ID_MANIPULATION, interactioncontext/INTERACTION_ID_MAX, interactioncontext/INTERACTION_ID_NONE, interactioncontext/INTERACTION_ID_SECONDARY_TAP, interactioncontext/INTERACTION_ID_TAP
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: INTERACTION_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERACTION_ID
 - interactioncontext/INTERACTION_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - INTERACTION_ID
---

# INTERACTION_ID enumeration


## -description

Specifies the interaction states used for configuring an <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object. Interactions can be static (single contact with no manipulation, such as tap, double tap, right tap, press and hold) or dynamic (one or more contacts with manipulation, such as translation, rotation, or scaling).

## -enum-fields

### -field INTERACTION_ID_NONE:0x00000000

Not used.

### -field INTERACTION_ID_MANIPULATION:0x00000001

A compound gesture that supports translation, rotation, and scaling (dynamic).

### -field INTERACTION_ID_TAP:0x00000002

A tap gesture (static).

### -field INTERACTION_ID_SECONDARY_TAP:0x00000003

A right click gesture (static), regardless of input device. Typically used for displaying a context menu.

<ul>
<li>Right mouse button click</li>
<li>Pen barrel button click</li>
<li>Touch or pen press and hold</li>
</ul>

### -field INTERACTION_ID_HOLD:0x00000004

Press and hold gesture (static).

### -field INTERACTION_ID_DRAG:0x00000005

Move with mouse or pen (dynamic).

### -field INTERACTION_ID_CROSS_SLIDE:0x00000006

Select or move through slide or swipe gestures (dynamic).

### -field INTERACTION_ID_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_configuration">INTERACTION_CONTEXT_CONFIGURATION</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext">SetInteractionConfigurationInteractionContext</a>
