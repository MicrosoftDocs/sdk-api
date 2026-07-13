---
UID: NN:inkrenderer.IInkD2DRenderer
title: IInkD2DRenderer (inkrenderer.h)
description: An IInkD2DRenderer object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default InkCanvas control.
helpviewer_keywords: ["IInkD2DRenderer","IInkD2DRenderer interface","IInkD2DRenderer interface","described","inkrenderer/IInkD2DRenderer","input_ink.iinkd2drenderer"]
old-location: input_ink\iinkd2drenderer.htm
tech.root: input_ink
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
ms.date: 03/21/2023
ms.keywords: IInkD2DRenderer, IInkD2DRenderer interface, IInkD2DRenderer interface,described, inkrenderer/IInkD2DRenderer, input_ink.iinkd2drenderer
req.header: inkrenderer.h
req.construct-type: iface
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
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
 - IInkD2DRenderer
 - inkrenderer/IInkD2DRenderer
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
 - IInkD2DRenderer
---

# IInkD2DRenderer interface

## -description

Enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [InkCanvas](/uwp/api/windows.ui.xaml.controls.inkcanvas) control.

## -inheritance

The **IInkD2DRenderer** interface inherits from the [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface. **IInkD2DRenderer** also has these types of members:

## -remarks

See the [IInkD2DRenderer::Draw](nf-inkrenderer-iinkd2drenderer-draw.md) method if you need to support Windows 11 contrast theme settings.

## -see-also

[IInkD2DRenderer2 interface](nn-inkrenderer-iinkd2drenderer2.md)
[Complex ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk)
[Simple ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk)
[Ink renderer interfaces](/windows/win32/input_ink/ink-renderer-interfaces)
[Pen and stylus interactions](/windows/uwp/input-and-devices/pen-and-stylus-interactions)
