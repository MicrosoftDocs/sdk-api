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

# INTERACTION_FLAGS enumeration


## -description


Specifies the state of an interaction.


## -enum-fields




### -field INTERACTION_FLAG_NONE

No flags set.


### -field INTERACTION_FLAG_BEGIN

The beginning of an interaction.


### -field INTERACTION_FLAG_END

The end of an interaction (including inertia).


### -field INTERACTION_FLAG_CANCEL

Interaction canceled. INTERACTION_FLAG_END also set on cancel.


### -field INTERACTION_FLAG_INERTIA

Inertia being processed.


### -field INTERACTION_FLAG_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/90ba531c-9f97-451d-8781-450dbc248f47">INTERACTION_CONTEXT_OUTPUT</a>



<a href="https://msdn.microsoft.com/7d2badad-5b98-4717-9409-5ee75d8fa213">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>



<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>



<a href="https://msdn.microsoft.com/87000250-f225-4864-96d2-1e189f5be1a3">RegisterOutputCallbackInteractionContext</a>
 

 

