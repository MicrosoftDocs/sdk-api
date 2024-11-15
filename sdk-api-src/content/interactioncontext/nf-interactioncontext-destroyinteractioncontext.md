---
UID: NF:interactioncontext.DestroyInteractionContext
title: DestroyInteractionContext function (interactioncontext.h)
description: Destroys the specified Interaction Context object.
helpviewer_keywords: ["DestroyInteractionContext","DestroyInteractionContext function","input_intcontext.destroyinteractioncontext","interactioncontext.destroyinteractioncontext","interactioncontext/DestroyInteractionContext"]
old-location: input_intcontext\destroyinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 871b35be-ccda-4a74-b516-e1e7f852782d
ms.date: 12/05/2018
ms.keywords: DestroyInteractionContext, DestroyInteractionContext function, input_intcontext.destroyinteractioncontext, interactioncontext.destroyinteractioncontext, interactioncontext/DestroyInteractionContext
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
 - DestroyInteractionContext
 - interactioncontext/DestroyInteractionContext
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
 - DestroyInteractionContext
---

# DestroyInteractionContext function


## -description

Destroys the specified [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -remarks

<b>DestroyInteractionContext</b> must be called to destroy any interaction context created by [CreateInteractionContext function](nf-interactioncontext-createinteractioncontext.md).

## -see-also












[ResetInteractionContext function](nf-interactioncontext-resetinteractioncontext.md)



[StopInteractionContext function](nf-interactioncontext-stopinteractioncontext.md)