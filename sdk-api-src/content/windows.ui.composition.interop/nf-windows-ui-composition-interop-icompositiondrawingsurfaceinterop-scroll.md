---
UID: NF:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop.Scroll
title: ICompositionDrawingSurfaceInterop::Scroll (windows.ui.composition.interop.h)
description: Scrolls a rectangular area of the logical surface.
helpviewer_keywords: ["ICompositionDrawingSurfaceInterop interface","Scroll method","ICompositionDrawingSurfaceInterop.Scroll","ICompositionDrawingSurfaceInterop.composition","ICompositionDrawingSurfaceInterop::Scroll","ICompositionDrawingSurfaceInterop::composition","Scroll","Scroll method","Scroll method","ICompositionDrawingSurfaceInterop interface","w_ui_comp.icompositiondrawingsurfaceinterop_scroll","windows/ICompositionDrawingSurfaceInterop::Scroll"]
old-location: w_ui_comp\icompositiondrawingsurfaceinterop_scroll.htm
tech.root: winrt
ms.assetid: 0FC12E3E-B104-4E61-817A-3F56C8DAC755
ms.date: 12/05/2018
ms.keywords: ICompositionDrawingSurfaceInterop interface,Scroll method, ICompositionDrawingSurfaceInterop.Scroll, ICompositionDrawingSurfaceInterop.composition, ICompositionDrawingSurfaceInterop::Scroll, ICompositionDrawingSurfaceInterop::composition, Scroll, Scroll method, Scroll method,ICompositionDrawingSurfaceInterop interface, w_ui_comp.icompositiondrawingsurfaceinterop_scroll, windows/ICompositionDrawingSurfaceInterop::Scroll
req.header: windows.ui.composition.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICompositionDrawingSurfaceInterop::Scroll
 - windows.ui.composition.interop/ICompositionDrawingSurfaceInterop::Scroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositionDrawingSurfaceInterop.Scroll
---

# ICompositionDrawingSurfaceInterop::Scroll (windows.ui.composition.interop.h)


## -description

Scrolls a rectangular area of the logical surface.

## -parameters

### -param scrollRect [in, optional]

Type: <b>const RECT*</b>

The rectangular area of the surface to be scrolled, relative to the upper-left corner of the surface. If this parameter is NULL, the entire surface is scrolled.

### -param clipRect [in, optional]

Type: <b>const RECT*</b>

The clipRect clips the destination (scrollRect after offset) of the scroll. The only bitmap content that will be scrolled are those that remain inside the clip rectangle after the scroll is completed.

### -param offsetX [in]

Type: <b>int</b>

The amount of horizontal scrolling, in pixels. Use positive values to scroll right, and negative values to scroll left.

### -param offsetY [in]

Type: <b>int</b>

The amount of vertical scrolling, in pixels. Use positive values to scroll down, and negative values to scroll up.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop">ICompositionDrawingSurfaceInterop</a>
