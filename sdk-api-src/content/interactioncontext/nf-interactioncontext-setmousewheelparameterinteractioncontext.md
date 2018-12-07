---
UID: NF:interactioncontext.SetMouseWheelParameterInteractionContext
title: SetMouseWheelParameterInteractionContext function
author: windows-sdk-content
description: Sets the parameter values for mouse wheel input.
old-location: input_intcontext\setmousewheelparameterinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: fbc47bd4-f78a-4b03-8adc-9b2c4620ea55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetMouseWheelParameterInteractionContext, SetMouseWheelParameterInteractionContext function, input_intcontext.setmousewheelparameterinteractioncontext, interactioncontext.setmousewheelparameterinteractioncontext, interactioncontext/SetMouseWheelParameterInteractionContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
api_name:
 - SetMouseWheelParameterInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetMouseWheelParameterInteractionContext function


## -description


Sets the parameter values for mouse wheel input. 


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


### -param value [in]

The value for <i>parameter</i>. 


### -param parameter [in]

One of the constants identified by <a href="https://msdn.microsoft.com/eafc5d3a-f547-45a2-9634-caf309e583f3">MOUSE_WHEEL_PARAMETER</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/2edb742d-a5a1-4c3b-bc0f-c119a2f1c221">GetMouseWheelParameterInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

