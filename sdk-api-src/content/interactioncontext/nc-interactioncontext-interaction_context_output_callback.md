---
UID: NC:interactioncontext.INTERACTION_CONTEXT_OUTPUT_CALLBACK
title: INTERACTION_CONTEXT_OUTPUT_CALLBACK (interactioncontext.h)
author: windows-sdk-content
description: Callback that receives events from an Interaction Context object.
old-location: input_intcontext\interaction_context_output_callback.htm
tech.root: Input_IntContext
ms.assetid: 7d2badad-5b98-4717-9409-5ee75d8fa213
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INTERACTION_CONTEXT_OUTPUT_CALLBACK, INTERACTION_CONTEXT_OUTPUT_CALLBACK callback, INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function, input_intcontext.interaction_context_output_callback, interactioncontext.interaction_context_output_callback, interactioncontext/INTERACTION_CONTEXT_OUTPUT_CALLBACK
ms.topic: callback
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
 - UserDefined
api_location:
 - interactioncontext.h
api_name:
 - INTERACTION_CONTEXT_OUTPUT_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function


## -description


Callback that receives events from an <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -parameters




### -param *clientData [in, optional]

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called.


### -param *output [in]

Output of the  <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/90ba531c-9f97-451d-8781-450dbc248f47">INTERACTION_CONTEXT_OUTPUT</a>



<a href="https://msdn.microsoft.com/DDD141E3-7DEE-4259-87BE-E11A51CF6EEE">Interaction Context Reference</a>



<a href="https://msdn.microsoft.com/87000250-f225-4864-96d2-1e189f5be1a3">RegisterOutputCallbackInteractionContext</a>
 

 

