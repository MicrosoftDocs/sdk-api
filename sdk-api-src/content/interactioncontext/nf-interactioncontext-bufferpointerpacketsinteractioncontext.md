---
UID: NF:interactioncontext.BufferPointerPacketsInteractionContext
title: BufferPointerPacketsInteractionContext function (interactioncontext.h)
description: Adds the history for a single input pointer to the buffer of the Interaction Context object.
helpviewer_keywords: ["BufferPointerPacketsInteractionContext","BufferPointerPacketsInteractionContext function","input_intcontext.bufferpointerpacketsinteractioncontext","interactioncontext.bufferpointerpacketsinteractioncontext","interactioncontext/BufferPointerPacketsInteractionContext"]
old-location: input_intcontext\bufferpointerpacketsinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: a76c87f9-5811-4a34-9843-f13a0592ddb4
ms.date: 12/05/2018
ms.keywords: BufferPointerPacketsInteractionContext, BufferPointerPacketsInteractionContext function, input_intcontext.bufferpointerpacketsinteractioncontext, interactioncontext.bufferpointerpacketsinteractioncontext, interactioncontext/BufferPointerPacketsInteractionContext
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
 - BufferPointerPacketsInteractionContext
 - interactioncontext/BufferPointerPacketsInteractionContext
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
 - BufferPointerPacketsInteractionContext
---

# BufferPointerPacketsInteractionContext function


## -description

Adds the history for a single input pointer to the buffer of the [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

### -param entriesCount [in]

The number of entries in the pointer history.

### -param pointerInfo [in]

Basic pointer information common to all pointer types.

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -see-also









[POINTER_INFO structure](../winuser/ns-winuser-pointer_info.md)