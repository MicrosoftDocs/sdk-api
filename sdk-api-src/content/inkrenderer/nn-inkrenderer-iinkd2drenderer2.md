---
UID: NN:inkrenderer.IInkD2DRenderer2
title: IInkD2DRenderer2 (inkrenderer.h)
description: An IInkD2DRenderer2 object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default InkCanvas control.
ms.date: 03/21/2023
ms.keywords: Draw, Draw method, Draw method,IInkD2DRenderer2 interface, IInkD2DRenderer2 interface,Draw method, IInkD2DRenderer2.Draw, IInkD2DRenderer2::Draw, inkrenderer/IInkD2DRenderer2::Draw, input_ink.iinkd2drenderer2_draw
tech.root: input_ink
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: inkrenderer.h
req.idl: Inkrenderer.idl
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.target-type: Windows
req.unicode-ansi: 
api_type:
 - COM
api_location:
 - inkrenderer.h
api_name:
 - IInkD2DRenderer2
f1_keywords:
 - IInkD2DRenderer2
 - inkrenderer/IInkD2DRenderer2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
helpviewer_keywords: ["IInkD2DRenderer2","Draw","Draw method","Draw method","IInkD2DRenderer2 interface","IInkD2DRenderer2 interface","Draw method","IInkD2DRenderer2.Draw","IInkD2DRenderer2::Draw","inkrenderer/IInkD2DRenderer2::Draw","input_ink.iinkd2drenderer2_draw"]
---

# IInkD2DRenderer2 interface

## -description

Enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [InkCanvas](/uwp/api/windows.ui.xaml.controls.inkcanvas) control.

## -inheritance

The **IInkD2DRenderer2** interface inherits from the [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface. **IInkD2DRenderer** also has these types of members:

## -remarks

This interface provides an overload of the [IInkD2DRenderer::Draw](nf-inkrenderer-iinkd2drenderer-draw.md) method to support contrast theme settings in Windows 11 and newer.

## -see-also

[IInkD2DRenderer interface](nn-inkrenderer-iinkd2drenderer.md)
[Complex ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk)
[Simple ink sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk)
[Ink renderer interfaces](/windows/win32/input_ink/ink-renderer-interfaces)
[Pen and stylus interactions](/windows/uwp/input-and-devices/pen-and-stylus-interactions)
