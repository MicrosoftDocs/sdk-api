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
 

 

