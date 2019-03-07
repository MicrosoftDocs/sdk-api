---
UID: NF:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop.Scroll
title: ICompositionDrawingSurfaceInterop::composition
author: windows-sdk-content
description: Scrolls a rectangular area of the logical surface.
old-location: w_ui_comp\icompositiondrawingsurfaceinterop_scroll.htm
tech.root: w_ui_comp
ms.assetid: 0FC12E3E-B104-4E61-817A-3F56C8DAC755
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICompositionDrawingSurfaceInterop interface,Scroll method, ICompositionDrawingSurfaceInterop.Scroll, ICompositionDrawingSurfaceInterop.composition, ICompositionDrawingSurfaceInterop::Scroll, ICompositionDrawingSurfaceInterop::composition, Scroll, Scroll method, Scroll method,ICompositionDrawingSurfaceInterop interface, w_ui_comp.icompositiondrawingsurfaceinterop_scroll, windows/ICompositionDrawingSurfaceInterop::Scroll
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositionDrawingSurfaceInterop.Scroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICompositionDrawingSurfaceInterop::composition


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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/C8A94128-009A-4327-8E77-A4E155D0910E">ICompositionDrawingSurfaceInterop</a>
 

 

