---
UID: NF:interactioncontext.ProcessBufferedPacketsInteractionContext
title: ProcessBufferedPacketsInteractionContext function (interactioncontext.h)
description: Process buffered packets at the end of a pointer input frame.
helpviewer_keywords: ["ProcessBufferedPacketsInteractionContext","ProcessBufferedPacketsInteractionContext function","input_intcontext.processbufferedpacketsinteractioncontext","interactioncontext.processbufferedpacketsinteractioncontext","interactioncontext/ProcessBufferedPacketsInteractionContext"]
old-location: input_intcontext\processbufferedpacketsinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 52bbeae9-70ab-403c-a035-de2acc2e0599
ms.date: 12/05/2018
ms.keywords: ProcessBufferedPacketsInteractionContext, ProcessBufferedPacketsInteractionContext function, input_intcontext.processbufferedpacketsinteractioncontext, interactioncontext.processbufferedpacketsinteractioncontext, interactioncontext/ProcessBufferedPacketsInteractionContext
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
 - ProcessBufferedPacketsInteractionContext
 - interactioncontext/ProcessBufferedPacketsInteractionContext
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
 - ProcessBufferedPacketsInteractionContext
---

# ProcessBufferedPacketsInteractionContext function

## -description

Process buffered packets at the end of a pointer input frame.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

**ProcessBufferedPacketsInteractionContext** is called at the end of the frame, when the buffer contains all the pointer histories from the frame.

## -see-also
