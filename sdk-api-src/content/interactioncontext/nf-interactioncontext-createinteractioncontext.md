---
UID: NF:interactioncontext.CreateInteractionContext
title: CreateInteractionContext function (interactioncontext.h)
description: Creates and initializes an Interaction Context object.
helpviewer_keywords: ["CreateInteractionContext","CreateInteractionContext function","input_intcontext.createinteractioncontext","interactioncontext.createinteractioncontext","interactioncontext/CreateInteractionContext"]
old-location: input_intcontext\createinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 90b81d1c-c1c0-442b-a534-f6e39e707230
ms.date: 12/05/2018
ms.keywords: CreateInteractionContext, CreateInteractionContext function, input_intcontext.createinteractioncontext, interactioncontext.createinteractioncontext, interactioncontext/CreateInteractionContext
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
 - CreateInteractionContext
 - interactioncontext/CreateInteractionContext
dev_langs:
 - c++
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
 - CreateInteractionContext
---

# CreateInteractionContext function


## -description

Creates and initializes an [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext [out]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -remarks

[DestroyInteractionContext function](nf-interactioncontext-destroyinteractioncontext.md) must be called to destroy any interaction context created by <b>CreateInteractionContext</b>.

## -see-also

[ResetInteractionContext function](nf-interactioncontext-resetinteractioncontext.md)



[StopInteractionContext function](nf-interactioncontext-stopinteractioncontext.md)