---
UID: NE:interactioncontext.INTERACTION_CONTEXT_PROPERTY
title: INTERACTION_CONTEXT_PROPERTY
author: windows-sdk-content
description: Specifies properties of the Interaction Context object.
old-location: input_intcontext\interaction_context_property.htm
tech.root: Input_IntContext
ms.assetid: b5b96b33-212e-4e1a-89f6-ee9f94de84aa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INTERACTION_CONTEXT_PROPERTY, INTERACTION_CONTEXT_PROPERTY enumeration, INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS, INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK, INTERACTION_CONTEXT_PROPERTY_MAX, INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS, input_intcontext.interaction_context_property, interactioncontext.interaction_context_property, interactioncontext/INTERACTION_CONTEXT_PROPERTY, interactioncontext/INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS, interactioncontext/INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK, interactioncontext/INTERACTION_CONTEXT_PROPERTY_MAX, interactioncontext/INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - INTERACTION_CONTEXT_PROPERTY
product: Windows
targetos: Windows
req.typenames: INTERACTION_CONTEXT_PROPERTY
req.redist: 
---

# INTERACTION_CONTEXT_PROPERTY enumeration


## -description


Specifies properties of the  <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object. 


## -enum-fields




### -field INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS

Measurement units used by the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object: himetric (0.01mm) or screen pixels.


### -field INTERACTION_CONTEXT_PROPERTY_INTERACTION_UI_FEEDBACK

UI feedback is provided.


### -field INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS

Pointer filtering is active.


### -field INTERACTION_CONTEXT_PROPERTY_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/c54a3632-aa7a-416b-b9ed-5ad552403985">GetPropertyInteractionContext</a>



<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>



<a href="https://msdn.microsoft.com/da24831e-9f9f-4a9f-92bf-60e1c5338554">SetPropertyInteractionContext</a>
 

 

