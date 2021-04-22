---
UID: NF:wingdi.wglGetLayerPaletteEntries
title: wglGetLayerPaletteEntries function (wingdi.h)
description: Retrieves the palette entries from a given color-index layer plane for a specified device context.
helpviewer_keywords: ["_ogl_wglGetLayerPaletteEntries","opengl.wglgetlayerpaletteentries","wglGetLayerPaletteEntries","wglGetLayerPaletteEntries function [OpenGL]","wingdi/wglGetLayerPaletteEntries"]
old-location: opengl\wglgetlayerpaletteentries.htm
tech.root: OpenGL
ms.assetid: 9f2d6f59-f1c6-44a5-8741-1ea4d84f5b2c
ms.date: 12/05/2018
ms.keywords: _ogl_wglGetLayerPaletteEntries, opengl.wglgetlayerpaletteentries, wglGetLayerPaletteEntries, wglGetLayerPaletteEntries function [OpenGL], wingdi/wglGetLayerPaletteEntries
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
 - wglGetLayerPaletteEntries
 - wingdi/wglGetLayerPaletteEntries
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
 - wglGetLayerPaletteEntries
---

# wglGetLayerPaletteEntries function


## -description

Retrieves the palette entries from a given color-index layer plane for a specified device context.

## -parameters

### -param unnamedParam1

Type: <b>HDC</b>

The device context of a window whose layer planes are to be described.

### -param unnamedParam2

Type: <b>int</b>

The overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure.

### -param unnamedParam3

Type: <b>int</b>

The first palette entry to be retrieved.

### -param unnamedParam4

Type: <b>int</b>

The number of palette entries to be retrieved.

### -param unnamedParam5

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a>*</b>

An array of structures that contain palette RGB color values. The array must contain at least as many structures as specified by <i>cEntries</i>.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the number of entries that were set in the palette in the specified layer plane of the window.

If the function fails or when no pixel format is selected, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Each color-index layer plane in a window has a palette with a size 2^<i>n</i>, where <i>n</i> is the number of bit planes in the layer plane. You cannot modify the transparent index of a palette.

Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette">wglRealizeLayerPalette</a> function to realize the layer palette. Initially the layer palette contains only entries for white.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-layerplanedescriptor">LAYERPLANEDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane">wglDescribeLayerPlane</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette">wglRealizeLayerPalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries">wglSetLayerPaletteEntries</a>