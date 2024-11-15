---
UID: NS:interactioncontext.CROSS_SLIDE_PARAMETER
title: CROSS_SLIDE_PARAMETER (interactioncontext.h)
description: Defines the cross-slide threshold and its distance threshold.
helpviewer_keywords: ["CROSS_SLIDE_PARAMETER","CROSS_SLIDE_PARAMETER structure","input_intcontext.cross_slide_parameter","interactioncontext.cross_slide_parameter","interactioncontext/CROSS_SLIDE_PARAMETER"]
old-location: input_intcontext\cross_slide_parameter.htm
tech.root: input_intcontext
ms.assetid: 3871f24e-34a4-4524-801d-4d60cf6165d9
ms.date: 12/05/2018
ms.keywords: CROSS_SLIDE_PARAMETER, CROSS_SLIDE_PARAMETER structure, input_intcontext.cross_slide_parameter, interactioncontext.cross_slide_parameter, interactioncontext/CROSS_SLIDE_PARAMETER
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CROSS_SLIDE_PARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CROSS_SLIDE_PARAMETER
 - interactioncontext/CROSS_SLIDE_PARAMETER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - CROSS_SLIDE_PARAMETER
---

# CROSS_SLIDE_PARAMETER structure

## -description

Defines the cross-slide threshold and its distance threshold.

## -struct-fields

### -field threshold

One of the constants from [CROSS_SLIDE_THRESHOLD enumeration](ne-interactioncontext-cross_slide_threshold.md).

### -field distance

The *threshold* distance, in DIPs.

## -see-also

[GetCrossSlideParameterInteractionContext function](nf-interactioncontext-getcrossslideparameterinteractioncontext.md)

[SetCrossSlideParametersInteractionContext function](nf-interactioncontext-setcrossslideparametersinteractioncontext.md)
