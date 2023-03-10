---
UID: NE:interactioncontext.CROSS_SLIDE_THRESHOLD
title: CROSS_SLIDE_THRESHOLD (interactioncontext.h)
description: Specifies the cross-slide behavior thresholds.
helpviewer_keywords: ["CROSS_SLIDE_THRESHOLD","CROSS_SLIDE_THRESHOLD enumeration","CROSS_SLIDE_THRESHOLD_COUNT","CROSS_SLIDE_THRESHOLD_MAX","CROSS_SLIDE_THRESHOLD_REARRANGE_START","CROSS_SLIDE_THRESHOLD_SELECT_START","CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END","CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START","input_intcontext.cross_slide_threshold","interactioncontext.cross_slide_threshold","interactioncontext/CROSS_SLIDE_THRESHOLD","interactioncontext/CROSS_SLIDE_THRESHOLD_COUNT","interactioncontext/CROSS_SLIDE_THRESHOLD_MAX","interactioncontext/CROSS_SLIDE_THRESHOLD_REARRANGE_START","interactioncontext/CROSS_SLIDE_THRESHOLD_SELECT_START","interactioncontext/CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END","interactioncontext/CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START"]
old-location: input_intcontext\cross_slide_threshold.htm
tech.root: input_intcontext
ms.assetid: c498e2ae-a761-4f93-9ec2-4030b03e64b9
ms.date: 12/05/2018
ms.keywords: CROSS_SLIDE_THRESHOLD, CROSS_SLIDE_THRESHOLD enumeration, CROSS_SLIDE_THRESHOLD_COUNT, CROSS_SLIDE_THRESHOLD_MAX, CROSS_SLIDE_THRESHOLD_REARRANGE_START, CROSS_SLIDE_THRESHOLD_SELECT_START, CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END, CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START, input_intcontext.cross_slide_threshold, interactioncontext.cross_slide_threshold, interactioncontext/CROSS_SLIDE_THRESHOLD, interactioncontext/CROSS_SLIDE_THRESHOLD_COUNT, interactioncontext/CROSS_SLIDE_THRESHOLD_MAX, interactioncontext/CROSS_SLIDE_THRESHOLD_REARRANGE_START, interactioncontext/CROSS_SLIDE_THRESHOLD_SELECT_START, interactioncontext/CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END, interactioncontext/CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START
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
req.typenames: CROSS_SLIDE_THRESHOLD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CROSS_SLIDE_THRESHOLD
 - interactioncontext/CROSS_SLIDE_THRESHOLD
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
 - CROSS_SLIDE_THRESHOLD
---

# CROSS_SLIDE_THRESHOLD enumeration


## -description

Specifies the cross-slide behavior thresholds.

## -enum-fields

### -field CROSS_SLIDE_THRESHOLD_SELECT_START:0x00000000

Selection start.

### -field CROSS_SLIDE_THRESHOLD_SPEED_BUMP_START:0x00000001

Speed bump start.

### -field CROSS_SLIDE_THRESHOLD_SPEED_BUMP_END:0x00000002

Speed bump end.

### -field CROSS_SLIDE_THRESHOLD_REARRANGE_START:0x00000003

Rearrange (drag and drop) start.

### -field CROSS_SLIDE_THRESHOLD_COUNT:0x00000004

The number of thresholds specified.

### -field CROSS_SLIDE_THRESHOLD_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-cross_slide_parameter">CROSS_SLIDE_PARAMETER</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext">GetCrossSlideParameterInteractionContext</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext">SetCrossSlideParametersInteractionContext</a>
