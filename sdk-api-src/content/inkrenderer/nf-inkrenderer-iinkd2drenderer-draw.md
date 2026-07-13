---
UID: NF:inkrenderer.IInkD2DRenderer.Draw
title: IInkD2DRenderer::Draw (inkrenderer.h)
description: Renders the ink stroke to the designated Direct2D device context of the app.
helpviewer_keywords: ["Draw","Draw method","Draw method","IInkD2DRenderer interface","IInkD2DRenderer interface","Draw method","IInkD2DRenderer.Draw","IInkD2DRenderer::Draw","inkrenderer/IInkD2DRenderer::Draw","input_ink.iinkd2drenderer_draw"]
old-location: input_ink\iinkd2drenderer_draw.htm
tech.root: input_ink
ms.assetid: 013f3b95-d5da-44e3-b2da-64a49cc8908e
ms.date: 03/21/2023
ms.keywords: Draw, Draw method, Draw method,IInkD2DRenderer interface, IInkD2DRenderer interface,Draw method, IInkD2DRenderer.Draw, IInkD2DRenderer::Draw, inkrenderer/IInkD2DRenderer::Draw, input_ink.iinkd2drenderer_draw
req.header: inkrenderer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inkrenderer.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkD2DRenderer::Draw
 - inkrenderer/IInkD2DRenderer::Draw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inkrenderer.h
api_name:
 - IInkD2DRenderer.Draw
---

# IInkD2DRenderer::Draw

## -description

Renders the ink stroke to the designated Direct2D device context of the app.

## -parameters

### -param pD2D1DeviceContext [in]

Pointer to the designated Direct2D device context of the app.

### -param pInkStrokeIterable [in]

Pointer to the collection of ink strokes to render.

### -param fHighContrast [in]

True, if the high-contrast accessibility option, in Windows 10 and earlier, is currently selected (Settings -> Ease of Access -> High Contrast -> Use high contrast). Otherwise, false.

Listen for the [HighContrastChanged](/uwp/api/windows.ui.viewmanagement.accessibilitysettings.highcontrastchanged) event to set this value appropriately.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[Complex ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk)
[Simple ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk)
[Ink renderer interfaces](/windows/win32/input_ink/ink-renderer-interfaces)
[Pen and stylus interactions](/windows/uwp/input-and-devices/pen-and-stylus-interactions)
