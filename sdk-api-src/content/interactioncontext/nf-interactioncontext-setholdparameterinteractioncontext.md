---
UID: NF:interactioncontext.SetHoldParameterInteractionContext
tech.root: input_intcontext
title: SetHoldParameterInteractionContext
ms.date: 06/28/2024
description: Sets the hold interaction behavior.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: interactioncontext.h
req.idl: 
req.include-header: 
req.irql: 
targetos: Windows
req.kmdf-ver: 
req.lib: ninput.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 21H1
req.target-min-winversvr: Windows Server 2022
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - SetHoldParameterInteractionContext
f1_keywords:
 - SetHoldParameterInteractionContext
 - interactioncontext/SetHoldParameterInteractionContext
dev_langs:
 - c++
helpviewer_keywords:
 - SetHoldParameterInteractionContext
---

# SetHoldParameterInteractionContext function

## -description

Sets the hold interaction behavior.

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

### -param parameter [in]

One of the constants from the [HOLD_PARAMETER enumeration](ne-interactioncontext-hold_parameter.md).

### -param value [out]

The value of *parameter*.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

## -see-also

[GetHoldParameterInteractionContext function](nf-interactioncontext-getholdparameterinteractioncontext.md)
