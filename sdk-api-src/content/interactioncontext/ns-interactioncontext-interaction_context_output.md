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
 

 

