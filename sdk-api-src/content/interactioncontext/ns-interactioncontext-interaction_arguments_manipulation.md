---
UID: NS:interactioncontext.INTERACTION_ARGUMENTS_MANIPULATION
title: INTERACTION_ARGUMENTS_MANIPULATION (interactioncontext.h)
author: windows-sdk-content
description: Defines the state of a manipulation.
old-location: input_intcontext\interaction_arguments_manipulation.htm
tech.root: Input_IntContext
ms.assetid: 8ef21f5a-51ae-4923-a5b4-0ee18bca563f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INTERACTION_ARGUMENTS_MANIPULATION, INTERACTION_ARGUMENTS_MANIPULATION structure, input_intcontext.interaction_arguments_manipulation, interactioncontext.interaction_arguments_manipulation, interactioncontext/INTERACTION_ARGUMENTS_MANIPULATION
ms.topic: struct
f1_keywords: 
 - "interactioncontext/INTERACTION_ARGUMENTS_MANIPULATION"
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
 - INTERACTION_ARGUMENTS_MANIPULATION
targetos: Windows
req.typenames: INTERACTION_ARGUMENTS_MANIPULATION
req.redist: 
ms.custom: 19H1
---

# INTERACTION_ARGUMENTS_MANIPULATION structure


## -description


Defines  the state of a manipulation.


## -struct-fields




### -field delta

The change in translation, rotation, and scale since the last <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nc-interactioncontext-interaction_context_output_callback">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>.


### -field cumulative

The accumulated change in translation, rotation, and scale since the interaction started.


### -field velocity

The velocities of the accumulated transformations for the interaction.


### -field railsState

One of the constants from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-manipulation_rails_state">MANIPULATION_RAILS_STATE</a>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_output">INTERACTION_CONTEXT_OUTPUT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/structures">Interaction Context Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext">RegisterOutputCallbackInteractionContext</a>
 

 

