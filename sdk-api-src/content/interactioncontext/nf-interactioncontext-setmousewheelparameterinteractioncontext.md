---
UID: NF:interactioncontext.SetMouseWheelParameterInteractionContext
title: SetMouseWheelParameterInteractionContext function (interactioncontext.h)
description: Sets the parameter values for mouse wheel input.
helpviewer_keywords: ["SetMouseWheelParameterInteractionContext","SetMouseWheelParameterInteractionContext function","input_intcontext.setmousewheelparameterinteractioncontext","interactioncontext.setmousewheelparameterinteractioncontext","interactioncontext/SetMouseWheelParameterInteractionContext"]
old-location: input_intcontext\setmousewheelparameterinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: fbc47bd4-f78a-4b03-8adc-9b2c4620ea55
ms.date: 12/05/2018
ms.keywords: SetMouseWheelParameterInteractionContext, SetMouseWheelParameterInteractionContext function, input_intcontext.setmousewheelparameterinteractioncontext, interactioncontext.setmousewheelparameterinteractioncontext, interactioncontext/SetMouseWheelParameterInteractionContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetMouseWheelParameterInteractionContext
 - interactioncontext/SetMouseWheelParameterInteractionContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
api_name:
 - SetMouseWheelParameterInteractionContext
---

# SetMouseWheelParameterInteractionContext function

## -description

Sets the parameter values for mouse wheel input.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

### -param value [in]

The value for *parameter*.

### -param parameter [in]

One of the constants identified by [MOUSE_WHEEL_PARAMETER enumeration](ne-interactioncontext-mouse_wheel_parameter.md).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[GetMouseWheelParameterInteractionContext function](nf-interactioncontext-getmousewheelparameterinteractioncontext.md)
