---
UID: NF:wingdi.wglGetLayerPaletteEntries
title: wglGetLayerPaletteEntries function
author: windows-sdk-content
description: Retrieves the palette entries from a given color-index layer plane for a specified device context.
old-location: opengl\wglgetlayerpaletteentries.htm
old-project: OpenGL
ms.assetid: 9f2d6f59-f1c6-44a5-8741-1ea4d84f5b2c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "_ogl_wglGetLayerPaletteEntries, opengl.wglgetlayerpaletteentries, wglGetLayerPaletteEntries, wglGetLayerPaletteEntries function [OpenGL], wingdi/wglGetLayerPaletteEntries"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	opengl32.dll
api_name:
-	wglGetLayerPaletteEntries
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wglGetLayerPaletteEntries function


## -description


Retrieves the palette entries from a given color-index layer plane for a specified device context.


## -parameters




### -param

TBD




#### - cEntries

Type: <b>int</b>

The number of palette entries to be retrieved.


#### - hdc

Type: <b>HDC</b>

The device context of a window whose layer planes are to be described.


#### - iLayerPlane

Type: <b>int</b>

The overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure.


#### - iStart

Type: <b>int</b>

The first palette entry to be retrieved.


#### - pcr

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

An array of structures that contain palette RGB color values. The array must contain at least as many structures as specified by <i>cEntries</i>.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of entries that were set in the palette in the specified layer plane of the window.

If the function fails or when no pixel format is selected, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Each color-index layer plane in a window has a palette with a size 2^<i>n</i>, where <i>n</i> is the number of bit planes in the layer plane. You cannot modify the transparent index of a palette.

Use the <a href="https://msdn.microsoft.com/083a563e-5b26-4ca8-8cae-c5a9ff901e8f">wglRealizeLayerPalette</a> function to realize the layer palette. Initially the layer palette contains only entries for white.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/fdb0322d-503f-4c17-b438-f764d60da7f6">LAYERPLANEDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/a80d257e-7053-4328-8298-80ed72513837">wglDescribeLayerPlane</a>



<a href="https://msdn.microsoft.com/083a563e-5b26-4ca8-8cae-c5a9ff901e8f">wglRealizeLayerPalette</a>



<a href="https://msdn.microsoft.com/bc44353d-15db-4e52-970d-a290b66bc046">wglSetLayerPaletteEntries</a>
 

 

