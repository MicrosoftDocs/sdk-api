---
UID: NF:interactioncontext.ProcessInertiaInteractionContext
title: ProcessInertiaInteractionContext function (interactioncontext.h)
description: Sends timer input to the Interaction Context object for inertia processing.
helpviewer_keywords: ["ProcessInertiaInteractionContext","ProcessInertiaInteractionContext function","input_intcontext.processinertiainteractioncontext","interactioncontext.processinertiainteractioncontext","interactioncontext/ProcessInertiaInteractionContext"]
old-location: input_intcontext\processinertiainteractioncontext.htm
tech.root: input_intcontext
ms.assetid: e1f18294-feb2-4340-8ed5-d76600c3d93a
ms.date: 12/05/2018
ms.keywords: ProcessInertiaInteractionContext, ProcessInertiaInteractionContext function, input_intcontext.processinertiainteractioncontext, interactioncontext.processinertiainteractioncontext, interactioncontext/ProcessInertiaInteractionContext
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
 - ProcessInertiaInteractionContext
 - interactioncontext/ProcessInertiaInteractionContext
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
 - ProcessInertiaInteractionContext
---

# ProcessInertiaInteractionContext function

## -description

Sends timer input to the [Interaction Context](../_input_intcontext/index.md) object for inertia processing.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

The caller is responsible for creating timer when inertia starts, and for driving inertia input with the timer by calling this function from the timer callback. Recommended timer period is 15 ms.

This function has no effect outside inertia.

## -see-also
