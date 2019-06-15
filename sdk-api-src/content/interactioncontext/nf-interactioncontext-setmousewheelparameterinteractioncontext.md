---
UID: NF:interactioncontext.SetMouseWheelParameterInteractionContext
title: SetMouseWheelParameterInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Sets the parameter values for mouse wheel input.
old-location: input_intcontext\setmousewheelparameterinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: fbc47bd4-f78a-4b03-8adc-9b2c4620ea55
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetMouseWheelParameterInteractionContext, SetMouseWheelParameterInteractionContext function, input_intcontext.setmousewheelparameterinteractioncontext, interactioncontext.setmousewheelparameterinteractioncontext, interactioncontext/SetMouseWheelParameterInteractionContext
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
ms.custom: 19H1
---

# SetMouseWheelParameterInteractionContext function


## -description


Sets the parameter values for mouse wheel input. 


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.


### -param value [in]

The value for <i>parameter</i>. 


### -param parameter [in]

One of the constants identified by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-mouse_wheel_parameter">MOUSE_WHEEL_PARAMETER</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext">GetMouseWheelParameterInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>
 

 

