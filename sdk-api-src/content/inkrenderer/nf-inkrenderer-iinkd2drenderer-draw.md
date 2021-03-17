---
UID: NF:inkrenderer.IInkD2DRenderer.Draw
title: IInkD2DRenderer::Draw (inkrenderer.h)
description: Renders the ink stroke to the designated Direct2D device context of the app.
helpviewer_keywords: ["Draw","Draw method","Draw method","IInkD2DRenderer interface","IInkD2DRenderer interface","Draw method","IInkD2DRenderer.Draw","IInkD2DRenderer::Draw","inkrenderer/IInkD2DRenderer::Draw","input_ink.iinkd2drenderer_draw"]
old-location: input_ink\iinkd2drenderer_draw.htm
tech.root: input_ink
ms.assetid: 013f3b95-d5da-44e3-b2da-64a49cc8908e
ms.date: 12/05/2018
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

Renders the ink stroke to the designated  Direct2D device context of the app.

## -parameters

### -param pD2D1DeviceContext [in]

Pointer to the designated Direct2D device context of the app.

### -param pInkStrokeIterable [in]

Pointer to the collection of ink strokes to render.

### -param fHighContrast [in]

True, if the Windows high-contrast accessibility option is currently selected. Otherwise, false.

Listen for the <a href="/uwp/api/windows.ui.viewmanagement.accessibilitysettings.highcontrastchanged">HighContrastChanged</a> event to set this value appropriately.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/windows/desktop/api/inkrenderer/nn-inkrenderer-iinkd2drenderer">IInkD2DRenderer</a>






<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>