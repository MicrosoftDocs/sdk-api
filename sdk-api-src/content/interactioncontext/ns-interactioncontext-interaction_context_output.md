---
UID: NS:interactioncontext.INTERACTION_CONTEXT_OUTPUT
title: INTERACTION_CONTEXT_OUTPUT (interactioncontext.h)
author: windows-sdk-content
description: Defines the output of the Interaction Context object.
old-location: input_intcontext\interaction_context_output.htm
tech.root: Input_IntContext
ms.assetid: 90ba531c-9f97-451d-8781-450dbc248f47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INTERACTION_CONTEXT_OUTPUT, INTERACTION_CONTEXT_OUTPUT structure, input_intcontext.interaction_context_output, interactioncontext.interaction_context_output, interactioncontext/INTERACTION_CONTEXT_OUTPUT
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
 - INTERACTION_CONTEXT_OUTPUT
product: Windows
targetos: Windows
req.typenames: INTERACTION_CONTEXT_OUTPUT
req.redist: 
ms.custom: 19H1
---

# INTERACTION_CONTEXT_OUTPUT structure


## -description


Defines the output of the  <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -struct-fields




### -field interactionId

ID of the  <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


### -field interactionFlags

One of the constants from <a href="https://msdn.microsoft.com/8d1adbd2-03ca-4609-9738-45bc7b21f934">INTERACTION_FLAGS</a>.


### -field inputType

One of the constants from <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">POINTER_INPUT_TYPE</a>.


### -field x

The x-coordinate of the input pointer, in HIMETRIC units.


### -field y

The y-coordinate of the input pointer, in HIMETRIC units.


### -field arguments


### -field arguments.manipulation

The state of the manipulation.


### -field arguments.tap

The state of the tap gesture.


### -field arguments.crossSlide

The state of the cross-slide interaction.


## -see-also




<a href="https://msdn.microsoft.com/365b0bed-888e-4e9c-ad13-254a241b9de9">INTERACTION_ARGUMENTS_CROSS_SLIDE</a>



<a href="https://msdn.microsoft.com/8ef21f5a-51ae-4923-a5b4-0ee18bca563f">INTERACTION_ARGUMENTS_MANIPULATION</a>



<a href="https://msdn.microsoft.com/162f35a0-5053-46ad-a7ca-ce314d584e34">INTERACTION_ARGUMENTS_TAP</a>



<a href="https://msdn.microsoft.com/7d2badad-5b98-4717-9409-5ee75d8fa213">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>



<a href="https://msdn.microsoft.com/8d1adbd2-03ca-4609-9738-45bc7b21f934">INTERACTION_FLAGS</a>



<a href="https://msdn.microsoft.com/38C5CE85-405B-455F-809D-19C77B8A217B">Interaction Context Structures</a>



<a href="https://msdn.microsoft.com/87000250-f225-4864-96d2-1e189f5be1a3">RegisterOutputCallbackInteractionContext</a>
 

 

