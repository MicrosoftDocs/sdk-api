---
UID: NF:interactioncontext.RemovePointerInteractionContext
title: RemovePointerInteractionContext function (interactioncontext.h)
description: Remove the specified pointer from the set of pointers processed by the Interaction Context object.
helpviewer_keywords: ["RemovePointerInteractionContext","RemovePointerInteractionContext function","input_intcontext.removepointerinteractioncontext","interactioncontext.removepointerinteractioncontext","interactioncontext/RemovePointerInteractionContext"]
old-location: input_intcontext\removepointerinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: d17f329b-f633-4aec-806f-3643206fce29
ms.date: 12/05/2018
ms.keywords: RemovePointerInteractionContext, RemovePointerInteractionContext function, input_intcontext.removepointerinteractioncontext, interactioncontext.removepointerinteractioncontext, interactioncontext/RemovePointerInteractionContext
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
 - RemovePointerInteractionContext
 - interactioncontext/RemovePointerInteractionContext
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
 - RemovePointerInteractionContext
---

# RemovePointerInteractionContext function

## -description

Remove the specified pointer from the set of pointers processed by the [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext [in]

Handle to the [Interaction Context](../_input_intcontext/index.md) object.

### -param pointerId [in]

ID of the pointer.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[AddPointerInteractionContext function](nf-interactioncontext-addpointerinteractioncontext.md)
