---
UID: NE:inkrenderer.__MIDL___MIDL_itf_inkrenderer_0000_0000_0001
tech.root: input_ink
title: INK_HIGH_CONTRAST_ADJUSTMENT (inkrenderer.h)
ms.date: 03/21/2023
ms.keywords: Draw, Draw method, Draw method,IInkD2DRenderer2 interface, IInkD2DRenderer2 interface,Draw method, IInkD2DRenderer2.Draw, IInkD2DRenderer2::Draw, inkrenderer/IInkD2DRenderer2::Draw, input_ink.iinkd2drenderer2_draw
targetos: Windows
description: Specifies how the IInkD2DRenderer2 object draws ink (standard and modified) when system is in a contrast theme mode.
helpviewer_keywords: ["INK_HIGH_CONTRAST_ADJUSTMENT","Draw","Draw method","Draw method","IInkD2DRenderer2 interface","IInkD2DRenderer2 interface","Draw method","IInkD2DRenderer2.Draw","IInkD2DRenderer2::Draw","inkrenderer/IInkD2DRenderer2::Draw","input_ink.iinkd2drenderer2_draw"]
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: inkrenderer.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - inkrenderer.h
api_name:
 - __MIDL___MIDL_itf_inkrenderer_0000_0000_0001
 - INK_HIGH_CONTRAST_ADJUSTMENT
f1_keywords:
 - __MIDL___MIDL_itf_inkrenderer_0000_0000_0001
 - inkrenderer/__MIDL___MIDL_itf_inkrenderer_0000_0000_0001
 - INK_HIGH_CONTRAST_ADJUSTMENT
 - inkrenderer/INK_HIGH_CONTRAST_ADJUSTMENT
dev_langs:
 - c++
---

# INK_HIGH_CONTRAST_ADJUSTMENT enum

## -description

Specifies how the [IInkD2DRenderer2](nn-inkrenderer-iinkd2drenderer2.md) object draws ink (standard and modified) when system is in a contrast theme mode.

## -enum-fields

### -field USE_SYSTEM_COLORS_WHEN_NECESSARY

For standard strokes, use selected color if contrast is sufficient against the background. Otherwise, use system color.

For highlighter strokes, use selected color if contrast is sufficient against the background. Otherwise, use system color.

### -field USE_SYSTEM_COLORS

For standard strokes, use system color.

For highlighter strokes, use system highlighter color.

### -field USE_ORIGINAL_COLORS

For standard strokes, use the selected color.

For highlighter strokes, use the selected color.

## -remarks

## -see-also

[Complex ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk)
[Simple ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk)
[Ink renderer interfaces](/windows/win32/input_ink/ink-renderer-interfaces)
[Pen and stylus interactions](/windows/uwp/input-and-devices/pen-and-stylus-interactions)
