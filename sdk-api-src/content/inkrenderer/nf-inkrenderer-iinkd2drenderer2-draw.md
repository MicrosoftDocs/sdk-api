---
UID: NF:inkrenderer.IInkD2DRenderer2.Draw
title: IInkD2DRenderer2::Draw (inkrenderer.h)
description: Renders the ink stroke to the designated Direct2D device context of the app.
helpviewer_keywords: ["Draw","Draw method","Draw method","IInkD2DRenderer2 interface","IInkD2DRenderer2 interface","Draw method","IInkD2DRenderer2.Draw","IInkD2DRenderer2::Draw","inkrenderer/IInkD2DRenderer2::Draw","input_ink.iinkd2drenderer2_draw"]
tech.root: input_ink
ms.date: 03/21/2023
ms.keywords: Draw, Draw method, Draw method,IInkD2DRenderer2 interface, IInkD2DRenderer2 interface,Draw method, IInkD2DRenderer2.Draw, IInkD2DRenderer2::Draw, inkrenderer/IInkD2DRenderer2::Draw, input_ink.iinkd2drenderer2_draw
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: inkrenderer.h
req.idl: Inkrenderer.idl
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - inkrenderer.h
api_name:
 - IInkD2DRenderer2::Draw
f1_keywords:
 - IInkD2DRenderer2::Draw
 - inkrenderer/IInkD2DRenderer2::Draw
dev_langs:
 - c++
---

## -description

Renders the ink stroke to the designated Direct2D device context of the app.

## -parameters

### -param pD2D1DeviceContext [in]

Pointer to the designated Direct2D device context of the app.

### -param pInkStrokeIterable [in]

Pointer to the collection of ink strokes to render.

### -param highContrastAdjustment

One of the values from the [INK_HIGH_CONTRAST_ADJUSTMENT enum](ne-inkrenderer-ink_high_contrast_adjustment.md).

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also

[Complex ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk)
[Simple ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk)
[Ink renderer interfaces](/windows/win32/input_ink/ink-renderer-interfaces)
[Pen and stylus interactions](/windows/uwp/input-and-devices/pen-and-stylus-interactions)
