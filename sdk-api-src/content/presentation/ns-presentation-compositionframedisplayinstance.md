---
UID: NS:presentation.CompositionFrameDisplayInstance
tech.root: comp_swapchain
title: CompositionFrameDisplayInstance
ms.date: 06/08/2021
targetos: Windows
description: Represents a single instance of the content shown on a single output.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: presentation.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: CompositionFrameDisplayInstance
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - CompositionFrameDisplayInstance
f1_keywords:
 - CompositionFrameDisplayInstance
 - presentation/CompositionFrameDisplayInstance
dev_langs:
 - c++
---

## -description

Represents a single instance of the content shown on a single output.

## -struct-fields

### -field outputAdapterLUID

Type: **LUID**

A locally unique ID (LUID) that refers to the display adapter (or output) that this instance corresponds to.

### -field outputVidPnSourceId

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

An integer that identifies a video present source on the display adapter (or output).

### -field outputUniqueId

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The unique ID of the display adapter (or output).

### -field instanceKind

Type: **[CompositionFrameInstanceKind](ne-presentation-compositionframeinstancekind.md)**

The kind of instance.

### -field finalTransform

Type: **[PresentationTransform](../presentationtypes/ns-presentationtypes-presentationtransform.md)**

The accumulated transform on screen of displayed content, including all transforms of ancestor visuals, if applicable.

### -field requiredCrossAdapterCopy

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` if a copy took place to display this instance due to the destination being a different adapter than the allocation's adapter; otherwise, `FALSE`.


### -field colorSpace

Type: **[DXGI_COLOR_SPACE_TYPE](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)**

The color space type of the output this instance was shown on.

## -remarks

## -see-also

