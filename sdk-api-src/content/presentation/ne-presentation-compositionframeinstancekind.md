---
UID: NE:presentation.CompositionFrameInstanceKind
tech.root: comp_swapchain
title: CompositionFrameInstanceKind
ms.date: 06/08/2021
targetos: Windows
description: Defines constants that indicate how the content was used in a composition frame.
prerelease: true
req.construct-type: enumeration
req.ddi-compliance: 
req.header: presentation.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - CompositionFrameInstanceKind
f1_keywords:
 - CompositionFrameInstanceKind
 - presentation/CompositionFrameInstanceKind
dev_langs:
 - c++
---

## -description

Defines constants that indicate how the content was used in a composition frame.

## -enum-fields

### -field CompositionFrameInstanceKind_ComposedOnScreen

Content was composed directly to the Desktop Window Manager (DWM) backbuffer.

### -field CompositionFrameInstanceKind_ScanoutOnScreen

Content was directly scanned out in an MPO plane.

### -field CompositionFrameInstanceKind_ComposedToIntermediate

Content was composed to an intermediate.

## -remarks

## -see-also

