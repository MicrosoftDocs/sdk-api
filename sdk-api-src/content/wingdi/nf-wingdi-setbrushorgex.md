---
UID: NF:wingdi.SetBrushOrgEx
title: SetBrushOrgEx function
author: windows-sdk-content
description: The SetBrushOrgEx function sets the brush origin that GDI assigns to the next brush an application selects into the specified device context.
old-location: gdi\setbrushorgex.htm
tech.root: gdi
ms.assetid: dcc7575a-49fd-4306-8baa-57e9e0d5ed1f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: SetBrushOrgEx, SetBrushOrgEx function [Windows GDI], _win32_SetBrushOrgEx, gdi.setbrushorgex, wingdi/SetBrushOrgEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetBrushOrgEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetBrushOrgEx function


## -description


The <b>SetBrushOrgEx</b> function sets the brush origin that GDI assigns to the next brush an application selects into the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The x-coordinate, in device units, of the new brush origin. If this value is greater than the brush width, its value is reduced using the modulus operator (<i>nXOrg</i> <b>mod</b> brush width).


### -param y [in]

The y-coordinate, in device units, of the new brush origin. If this value is greater than the brush height, its value is reduced using the modulus operator (<i>nYOrg</i> <b>mod</b> brush height).


### -param lppt [out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the previous brush origin.

This parameter can be <b>NULL</b> if the previous brush origin is not required.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



A brush is a bitmap that the system uses to paint the interiors of filled shapes.

The brush origin is a pair of coordinates specifying the location of one pixel in the bitmap. The default brush origin coordinates are (0,0). For horizontal coordinates, the value 0 corresponds to the leftmost column of pixels; the width corresponds to the rightmost column. For vertical coordinates, the value 0 corresponds to the uppermost row of pixels; the height corresponds to the lowermost row.

The system automatically tracks the origin of all window-managed device contexts and adjusts their brushes as necessary to maintain an alignment of patterns on the surface. The brush origin that is set with this call is relative to the upper-left corner of the client area.

An application should call <b>SetBrushOrgEx</b> after setting the bitmap stretching mode to HALFTONE by using <a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>. This must be done to avoid brush misalignment.

The system automatically tracks the origin of all window-managed device contexts and adjusts their brushes as necessary to maintain an alignment of patterns on the surface.




## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/0b938237-cb06-4776-86f8-14478abcee00">GetBrushOrgEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>



<a href="https://msdn.microsoft.com/b84cd0b3-fdf1-4f12-bc45-308032d6d698">UnrealizeObject</a>
 

 

