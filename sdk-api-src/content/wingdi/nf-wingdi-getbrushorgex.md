---
UID: NF:wingdi.GetBrushOrgEx
title: GetBrushOrgEx function
author: windows-sdk-content
description: The GetBrushOrgEx function retrieves the current brush origin for the specified device context. This function replaces the GetBrushOrg function.
old-location: gdi\getbrushorgex.htm
tech.root: gdi
ms.assetid: 0b938237-cb06-4776-86f8-14478abcee00
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetBrushOrgEx, GetBrushOrgEx function [Windows GDI], _win32_GetBrushOrgEx, gdi.getbrushorgex, wingdi/GetBrushOrgEx
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
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetBrushOrgEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetBrushOrgEx function


## -description


The <b>GetBrushOrgEx</b> function retrieves the current brush origin for the specified device context. This function replaces the <b>GetBrushOrg</b> function.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lppt [out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the brush origin, in device coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



A brush is a bitmap that the system uses to paint the interiors of filled shapes.

The brush origin is a set of coordinates with values between 0 and 7, specifying the location of one pixel in the bitmap. The default brush origin coordinates are (0,0). For horizontal coordinates, the value 0 corresponds to the leftmost column of pixels; the value 7 corresponds to the rightmost column. For vertical coordinates, the value 0 corresponds to the uppermost row of pixels; the value 7 corresponds to the lowermost row. When the system positions the brush at the start of any painting operation, it maps the origin of the brush to the location in the window's client area specified by the brush origin. For example, if the origin is set to (2,3), the system maps the origin of the brush (0,0) to the location (2,3) on the window's client area.

If an application uses a brush to fill the backgrounds of both a parent and a child window with matching colors, it may be necessary to set the brush origin after painting the parent window but before painting the child window.

The system automatically tracks the origin of all window-managed device contexts and adjusts their brushes as necessary to maintain an alignment of patterns on the surface.




## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>



<a href="https://msdn.microsoft.com/b84cd0b3-fdf1-4f12-bc45-308032d6d698">UnrealizeObject</a>
 

 

