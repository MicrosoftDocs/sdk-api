---
UID: NF:interactioncontext.SetPivotInteractionContext
title: SetPivotInteractionContext function (interactioncontext.h)
description: Sets the center point, and the pivot radius from the center point, for a rotation manipulation using a single input pointer.
helpviewer_keywords: ["SetPivotInteractionContext","SetPivotInteractionContext function","input_intcontext.setpivotinteractioncontext","interactioncontext.setpivotinteractioncontext","interactioncontext/SetPivotInteractionContext"]
old-location: input_intcontext\setpivotinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 3997e444-e90a-417f-a75c-69363b4c82d2
ms.date: 12/05/2018
ms.keywords: SetPivotInteractionContext, SetPivotInteractionContext function, input_intcontext.setpivotinteractioncontext, interactioncontext.setpivotinteractioncontext, interactioncontext/SetPivotInteractionContext
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
 - SetPivotInteractionContext
 - interactioncontext/SetPivotInteractionContext
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
 - SetPivotInteractionContext
---

# SetPivotInteractionContext function

## -description

Sets the center point, and the pivot radius from the center point, for a rotation manipulation using a single input pointer.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

### -param x [in]

The x-coordinate for the screen location of the center point.

### -param y [in]

The y-coordinate for the screen location of the center point.

### -param radius [in]

The offset between the center point and the single input pointer, in HIMETRIC units.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also
