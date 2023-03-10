---
UID: NF:wingdi.wglRealizeLayerPalette
title: wglRealizeLayerPalette function (wingdi.h)
description: The wglRealizeLayerPalette function maps palette entries from a given color-index layer plane into the physical palette or initializes the palette of an RGBA layer plane.
helpviewer_keywords: ["_ogl_wglRealizeLayerPalette","opengl.wglrealizelayerpalette","wglRealizeLayerPalette","wglRealizeLayerPalette function [OpenGL]","wingdi/wglRealizeLayerPalette"]
old-location: opengl\wglrealizelayerpalette.htm
tech.root: OpenGL
ms.assetid: 083a563e-5b26-4ca8-8cae-c5a9ff901e8f
ms.date: 12/05/2018
ms.keywords: _ogl_wglRealizeLayerPalette, opengl.wglrealizelayerpalette, wglRealizeLayerPalette, wglRealizeLayerPalette function [OpenGL], wingdi/wglRealizeLayerPalette
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wglRealizeLayerPalette
 - wingdi/wglRealizeLayerPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglRealizeLayerPalette
---

# wglRealizeLayerPalette function


## -description

The <b>wglRealizeLayerPalette</b> function maps palette entries from a given color-index layer plane into the physical palette or initializes the palette of an RGBA layer plane.

## -parameters

### -param unnamedParam1

Specifies the device context of a window whose layer plane palette is to be realized into the physical palette.

### -param unnamedParam2

Specifies the overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure.

### -param unnamedParam3

Indicates whether the palette is to be realized into the physical palette. When <i>bRealize</i> is <b>TRUE</b>, the palette entries are mapped into the physical palette where available. When <i>bRealize</i> is <b>FALSE</b>, the palette entries for the layer plane of the window are no longer needed and might be released for use by another foreground window.

## -returns

If the function succeeds, the return value is <b>TRUE</b>, even if <i>bRealize</i> is <b>TRUE</b> and the physical palette is not available. If the function fails or when no pixel format is selected, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The physical palette for a layer plane is a shared resource among windows with layer planes. When more than one window attempts to realize a palette for a given physical layer plane, only one palette at a time is realized. When you call the <b>wglRealizeLayerPalette</b> function, the layer palette of a foreground window is always realized first.

When a window's layer palette is realized, its palette entries are always mapped one-to-one into the physical palette. Unlike GDI logical palettes, with <b>wglRealizeLayerPalette</b> there is no mapping of other windows' layer palettes to the current physical palette.

Whenever a window becomes the foreground window, call <b>wglRealizeLayerPalette</b> to realize its layer palettes again, even if the pixel type of the layer plane is RGBA.

Because <b>wglRealizeLayerPalette</b> doesn't realize the palette of the main plane, use GDI palette functions to realize the main plane palette.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-layerplanedescriptor">LAYERPLANEDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane">wglDescribeLayerPlane</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries">wglGetLayerPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette">wglRealizeLayerPalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries">wglSetLayerPaletteEntries</a>