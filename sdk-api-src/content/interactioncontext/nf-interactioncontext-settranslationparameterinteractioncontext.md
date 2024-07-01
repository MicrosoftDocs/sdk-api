---
UID: NF:interactioncontext.SetTranslationParameterInteractionContext
tech.root: input_intcontext
title: SetTranslationParameterInteractionContext
ms.date: 06/28/2024
description: Sets the drag interaction behavior.
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
req.lib: 
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
 - SetTranslationParameterInteractionContext
f1_keywords:
 - SetTranslationParameterInteractionContext
 - interactioncontext/SetTranslationParameterInteractionContext
dev_langs:
 - c++
helpviewer_keywords:
 - SetTranslationParameterInteractionContext
---

# SetTranslationParameterInteractionContext function

## -description

Sets the drag interaction behavior.

## -parameters

### -param interactionContext

The handle of the interaction context.

### -param parameter

One of the constants from the [TRANSLATION_PARAMETER enumeration](ne-interactioncontext-translation_parameter.md).

### -param value

The value of *parameter*.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

## -see-also

[GetTranslationParameterInteractionContext function](nf-interactioncontext-gettranslationparameterinteractioncontext.md)
