---
UID: NF:wingdi.wglSetLayerPaletteEntries
title: wglSetLayerPaletteEntries function (wingdi.h)
description: Sets the palette entries in a given color-index layer plane for a specified device context.
helpviewer_keywords: ["_ogl_wglSetLayerPaletteEntries","opengl.wglsetlayerpaletteentries","wglSetLayerPaletteEntries","wglSetLayerPaletteEntries function [OpenGL]","wingdi/wglSetLayerPaletteEntries"]
old-location: opengl\wglsetlayerpaletteentries.htm
tech.root: OpenGL
ms.assetid: bc44353d-15db-4e52-970d-a290b66bc046
ms.date: 12/05/2018
ms.keywords: _ogl_wglSetLayerPaletteEntries, opengl.wglsetlayerpaletteentries, wglSetLayerPaletteEntries, wglSetLayerPaletteEntries function [OpenGL], wingdi/wglSetLayerPaletteEntries
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
 - wglSetLayerPaletteEntries
 - wingdi/wglSetLayerPaletteEntries
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
 - wglSetLayerPaletteEntries
---

# wglSetLayerPaletteEntries function


## -description

Sets the palette entries in a given color-index layer plane for a specified device context.

## -parameters

### -param unnamedParam1

Type: <b>HDC</b>

The device context of a window whose layer palette is to be set.

### -param unnamedParam2

Type: <b>int</b>

An overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure.

### -param unnamedParam3

Type: <b>int</b>

The first palette entry to be set.

### -param unnamedParam4

Type: <b>int</b>

The number of palette entries to be set.

### -param unnamedParam5

Type: <b>const <a href="/windows/desktop/gdi/colorref">COLORREF</a>*</b>

A pointer to the first member of an array of <i>cEntries</i> structures that contain RGB color information.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the number of entries that were set in the palette in the specified layer plane of the window. If the function fails or no pixel format is selected, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Each color-index plane in a window has a palette with a size 2^n, where <i>n</i> is the number of bit planes in the layer plane. You cannot modify the transparent index of a palette.

Use the <b>wglRealizeLayerPalette</b> function to realize the layer palette. Initially the layer palette contains only entries for white.

The <b>wglSetLayerPaletteEntries</b> function doesn't set the palette entries of the main plane palette. To update the main plane palette, use GDI palette functions.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-layerplanedescriptor">LAYERPLANEDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane">wglDescribeLayerPlane</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries">wglGetLayerPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette">wglRealizeLayerPalette</a>