---
UID: NF:interactioncontext.SetCrossSlideParametersInteractionContext
title: SetCrossSlideParametersInteractionContext function (interactioncontext.h)
description: Configures the cross-slide interaction.
helpviewer_keywords: ["SetCrossSlideParametersInteractionContext","SetCrossSlideParametersInteractionContext function","input_intcontext.setcrossslideparametersinteractioncontext","interactioncontext.setcrossslideparametersinteractioncontext","interactioncontext/SetCrossSlideParametersInteractionContext"]
old-location: input_intcontext\setcrossslideparametersinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: b4d9459a-7b07-4316-bf5c-628de08de7dc
ms.date: 12/05/2018
ms.keywords: SetCrossSlideParametersInteractionContext, SetCrossSlideParametersInteractionContext function, input_intcontext.setcrossslideparametersinteractioncontext, interactioncontext.setcrossslideparametersinteractioncontext, interactioncontext/SetCrossSlideParametersInteractionContext
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
 - SetCrossSlideParametersInteractionContext
 - interactioncontext/SetCrossSlideParametersInteractionContext
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
 - SetCrossSlideParametersInteractionContext
---

# SetCrossSlideParametersInteractionContext function

## -description

Configures the cross-slide interaction.

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

### -param parameterCount [in]

Number of parameters to set.

### -param crossSlideParameters [in]

The cross-slide threshold and its distance threshold.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

**SetCrossSlideParametersInteractionContext** fails if a [CROSS_SLIDE_PARAMETER structure](ns-interactioncontext-cross_slide_parameter.md) is enabled, but not specified  in the *crossSlideParameters* parameter.

### Examples

This example demonstrates how to set custom cross-slide thresholds.

```cpp
//  SetCrossSlideParametersInteractionContext

CROSS_SLIDE_PARAMETER crossSlideParameters[4];
crossSlideParameters[0].threshold = CROSS_SLIDE_THRESHOLD_SELECT_START;
crossSlideParameters[0].distance = customSelectStart;
crossSlideParameters[1].threshold = CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START;
crossSlideParameters[1].distance = customSpeedBumpStart;
crossSlideParameters[2].threshold = CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END;
crossSlideParameters[2].distance = customSpeedBumpEnd;
crossSlideParameters[3].threshold = CROSS_SLIDE_THRESHOLD_REARRANGE_START;
crossSlideParameters[3].distance = customRearrangeStart;

// set thresholds for select, speedbump, and rearrange
SetCrossSlideParametersInteractionContext(
    m_interactionContext,
    4,
    crossSlideParameters);
```

## -see-also

[CROSS_SLIDE_PARAMETER structure](ns-interactioncontext-cross_slide_parameter.md)

[GetCrossSlideParameterInteractionContext function](nf-interactioncontext-getcrossslideparameterinteractioncontext.md)
