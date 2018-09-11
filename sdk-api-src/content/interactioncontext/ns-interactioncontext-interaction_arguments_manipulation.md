---
UID: NS:interactioncontext.INTERACTION_ARGUMENTS_MANIPULATION
title: INTERACTION_ARGUMENTS_MANIPULATION
author: windows-sdk-content
description: Defines the state of a manipulation.
old-location: input_intcontext\interaction_arguments_manipulation.htm
tech.root: Input_IntContext
ms.assetid: 8ef21f5a-51ae-4923-a5b4-0ee18bca563f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: INTERACTION_ARGUMENTS_MANIPULATION, INTERACTION_ARGUMENTS_MANIPULATION structure, input_intcontext.interaction_arguments_manipulation, interactioncontext.interaction_arguments_manipulation, interactioncontext/INTERACTION_ARGUMENTS_MANIPULATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: INTERACTION_ARGUMENTS_MANIPULATION
req.redist: 
---

# INTERACTION_ARGUMENTS_MANIPULATION structure


## -description


Defines  the state of a manipulation.


## -struct-fields




### -field delta

The change in translation, rotation, and scale since the last <a href="https://msdn.microsoft.com/7d2badad-5b98-4717-9409-5ee75d8fa213">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>.


### -field cumulative

The accumulated change in translation, rotation, and scale since the interaction started.


### -field velocity

The velocities of the accumulated transformations for the interaction.


### -field railsState

One of the constants from <a href="https://msdn.microsoft.com/b4978408-e124-482e-b552-7a6db76a40ad">MANIPULATION_RAILS_STATE</a>.


## -see-also




<a href="https://msdn.microsoft.com/90ba531c-9f97-451d-8781-450dbc248f47">INTERACTION_CONTEXT_OUTPUT</a>



<a href="https://msdn.microsoft.com/38C5CE85-405B-455F-809D-19C77B8A217B">Interaction Context Structures</a>



<a href="https://msdn.microsoft.com/87000250-f225-4864-96d2-1e189f5be1a3">RegisterOutputCallbackInteractionContext</a>
 

 

