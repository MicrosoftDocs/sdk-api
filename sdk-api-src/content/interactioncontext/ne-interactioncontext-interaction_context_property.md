---
UID: NE:interactioncontext.INTERACTION_CONTEXT_PROPERTY
title: INTERACTION_CONTEXT_PROPERTY (interactioncontext.h)
description: Specifies properties of the Interaction Context object.
helpviewer_keywords: ["INTERACTION_CONTEXT_PROPERTY","INTERACTION_CONTEXT_PROPERTY enumeration","INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS","INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK","INTERACTION_CONTEXT_PROPERTY_MAX","INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS","input_intcontext.interaction_context_property","interactioncontext.interaction_context_property","interactioncontext/INTERACTION_CONTEXT_PROPERTY","interactioncontext/INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS","interactioncontext/INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK","interactioncontext/INTERACTION_CONTEXT_PROPERTY_MAX","interactioncontext/INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS"]
old-location: input_intcontext\interaction_context_property.htm
tech.root: input_intcontext
ms.assetid: b5b96b33-212e-4e1a-89f6-ee9f94de84aa
ms.date: 12/05/2018
ms.keywords: INTERACTION_CONTEXT_PROPERTY, INTERACTION_CONTEXT_PROPERTY enumeration, INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS, INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK, INTERACTION_CONTEXT_PROPERTY_MAX, INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS, input_intcontext.interaction_context_property, interactioncontext.interaction_context_property, interactioncontext/INTERACTION_CONTEXT_PROPERTY, interactioncontext/INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS, interactioncontext/INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK, interactioncontext/INTERACTION_CONTEXT_PROPERTY_MAX, interactioncontext/INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS
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
req.typenames: INTERACTION_CONTEXT_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERACTION_CONTEXT_PROPERTY
 - interactioncontext/INTERACTION_CONTEXT_PROPERTY
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
 - INTERACTION_CONTEXT_PROPERTY
---

# INTERACTION_CONTEXT_PROPERTY enumeration


## -description

Specifies properties of the  <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

## -enum-fields

### -field INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS:0x00000001

Measurement units used by the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object: himetric (0.01mm) or screen pixels.

### -field INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK:0x00000002

UI feedback is provided.

### -field INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS:0x00000003

Pointer filtering is active.

### -field INTERACTION_CONTEXT_PROPERTY_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext">GetPropertyInteractionContext</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext">SetPropertyInteractionContext</a>
