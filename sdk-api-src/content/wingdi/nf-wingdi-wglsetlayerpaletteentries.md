---
UID: NF:wingdi.wglSetLayerPaletteEntries
title: wglSetLayerPaletteEntries function
author: windows-sdk-content
description: Sets the palette entries in a given color-index layer plane for a specified device context.
old-location: opengl\wglsetlayerpaletteentries.htm
tech.root: OpenGL
ms.assetid: bc44353d-15db-4e52-970d-a290b66bc046
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ogl_wglSetLayerPaletteEntries, opengl.wglsetlayerpaletteentries, wglSetLayerPaletteEntries, wglSetLayerPaletteEntries function [OpenGL], wingdi/wglSetLayerPaletteEntries"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglSetLayerPaletteEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- wglSetLayerPaletteEntries
: 
---

# wglSetLayerPaletteEntries function


## -description


Sets the palette entries in a given color-index layer plane for a specified device context.


## -parameters




### -param arg1

Type: <b>HDC</b>

The device context of a window whose layer palette is to be set.


### -param arg2

Type: <b>int</b>

An overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure.


### -param arg3

Type: <b>int</b>

The first palette entry to be set.


### -param arg4

Type: <b>int</b>

The number of palette entries to be set.


### -param arg5

Type: <b>const <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

A pointer to the first member of an array of <i>cEntries</i> structures that contain RGB color information.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of entries that were set in the palette in the specified layer plane of the window. If the function fails or no pixel format is selected, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Each color-index plane in a window has a palette with a size 2^n, where <i>n</i> is the number of bit planes in the layer plane. You cannot modify the transparent index of a palette.

Use the <b>wglRealizeLayerPalette</b> function to realize the layer palette. Initially the layer palette contains only entries for white.

The <b>wglSetLayerPaletteEntries</b> function doesn't set the palette entries of the main plane palette. To update the main plane palette, use GDI palette functions.




## -see-also




<a href="https://msdn.microsoft.com/fdb0322d-503f-4c17-b438-f764d60da7f6">LAYERPLANEDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/a80d257e-7053-4328-8298-80ed72513837">wglDescribeLayerPlane</a>



<a href="https://msdn.microsoft.com/9f2d6f59-f1c6-44a5-8741-1ea4d84f5b2c">wglGetLayerPaletteEntries</a>



<a href="https://msdn.microsoft.com/083a563e-5b26-4ca8-8cae-c5a9ff901e8f">wglRealizeLayerPalette</a>
 

 

