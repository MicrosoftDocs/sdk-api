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
 

 

