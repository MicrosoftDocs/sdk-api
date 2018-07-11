---
UID: NF:interactioncontext.RegisterOutputCallbackInteractionContext
title: RegisterOutputCallbackInteractionContext function
author: windows-sdk-content
description: Registers a callback to receive interaction events from an Interaction Context object.
old-location: input_intcontext\registeroutputcallbackinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: 87000250-f225-4864-96d2-1e189f5be1a3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: RegisterOutputCallbackInteractionContext, RegisterOutputCallbackInteractionContext function, input_intcontext.registeroutputcallbackinteractioncontext, interactioncontext.registeroutputcallbackinteractioncontext, interactioncontext/RegisterOutputCallbackInteractionContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MOUSE_WHEEL_PARAMETER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
 - API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
 - IE_Shims.dll
api_name:
 - RegisterOutputCallbackInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# RegisterOutputCallbackInteractionContext function


## -description


Registers a callback to receive interaction events from an <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

Handle to the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


### -param outputCallback [in]

The callback function.


### -param clientData [in, optional]

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called (<b>this</b>).


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



Each instance of an <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> is limited to one output callback. Registering a callback function overwrites any existing callback registration for the Interaction Context.

This function is typically called after the creation of an <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> or when the Interaction Context is reassigned to another UI element.




## -see-also




<a href="https://msdn.microsoft.com/90ba531c-9f97-451d-8781-450dbc248f47">INTERACTION_CONTEXT_OUTPUT</a>



<a href="https://msdn.microsoft.com/7d2badad-5b98-4717-9409-5ee75d8fa213">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

