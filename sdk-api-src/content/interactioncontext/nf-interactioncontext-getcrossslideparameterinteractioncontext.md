---
UID: NF:interactioncontext.GetCrossSlideParameterInteractionContext
title: GetCrossSlideParameterInteractionContext function (interactioncontext.h)
description: Gets the cross-slide interaction behavior.
helpviewer_keywords: ["GetCrossSlideParameterInteractionContext","GetCrossSlideParameterInteractionContext function","input_intcontext.getcrossslideparameterinteractioncontext","interactioncontext.getcrossslideparameterinteractioncontext","interactioncontext/GetCrossSlideParameterInteractionContext"]
old-location: input_intcontext\getcrossslideparameterinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 19e934c6-8cd7-4302-a903-bd7865aef908
ms.date: 12/05/2018
ms.keywords: GetCrossSlideParameterInteractionContext, GetCrossSlideParameterInteractionContext function, input_intcontext.getcrossslideparameterinteractioncontext, interactioncontext.getcrossslideparameterinteractioncontext, interactioncontext/GetCrossSlideParameterInteractionContext
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
 - GetCrossSlideParameterInteractionContext
 - interactioncontext/GetCrossSlideParameterInteractionContext
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
 - GetCrossSlideParameterInteractionContext
---

# GetCrossSlideParameterInteractionContext function

## -description

Gets the cross-slide interaction behavior.

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

### -param threshold [in]

One of the constants from [CROSS_SLIDE_THRESHOLD enumeration](ne-interactioncontext-cross_slide_threshold.md).

### -param distance [out]

The distance threshold of *threshold*.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[CROSS_SLIDE_PARAMETER structure](ns-interactioncontext-cross_slide_parameter.md)

[SetCrossSlideParametersInteractionContext function](nf-interactioncontext-setcrossslideparametersinteractioncontext.md)
