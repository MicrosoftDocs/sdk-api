---
UID: NF:interactioncontext.GetMouseWheelParameterInteractionContext
title: GetMouseWheelParameterInteractionContext function (interactioncontext.h)
description: Gets the mouse wheel state for the Interaction Context object.
helpviewer_keywords: ["GetMouseWheelParameterInteractionContext","GetMouseWheelParameterInteractionContext function","input_intcontext.getmousewheelparameterinteractioncontext","interactioncontext.getmousewheelparameterinteractioncontext","interactioncontext/GetMouseWheelParameterInteractionContext"]
old-location: input_intcontext\getmousewheelparameterinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 2edb742d-a5a1-4c3b-bc0f-c119a2f1c221
ms.date: 12/05/2018
ms.keywords: GetMouseWheelParameterInteractionContext, GetMouseWheelParameterInteractionContext function, input_intcontext.getmousewheelparameterinteractioncontext, interactioncontext.getmousewheelparameterinteractioncontext, interactioncontext/GetMouseWheelParameterInteractionContext
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
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMouseWheelParameterInteractionContext
 - interactioncontext/GetMouseWheelParameterInteractionContext
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
 - GetMouseWheelParameterInteractionContext
---

# GetMouseWheelParameterInteractionContext function

## -description

Gets the mouse wheel state for the [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

### -param value [out]

The value of *parameter*.

### -param parameter [in]

One of the constants from [MOUSE_WHEEL_PARAMETER enumeration](ne-interactioncontext-mouse_wheel_parameter.md).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[SetMouseWheelParameterInteractionContext function](nf-interactioncontext-setmousewheelparameterinteractioncontext.md)
