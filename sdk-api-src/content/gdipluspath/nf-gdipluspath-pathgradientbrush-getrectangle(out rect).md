---
UID: NF:gdipluspath.PathGradientBrush.GetRectangle(OUT Rect)
title: PathGradientBrush::GetRectangle(OUT Rect)
author: windows-sdk-content
description: The PathGradientBrush::GetRectangle method gets the smallest rectangle that encloses the boundary path of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushgetrectanglemethods\getrectangle_89rectrect.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetRectangle, GetRectangle method [GDI+], GetRectangle method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetRectangle method, PathGradientBrush.GetRectangle, PathGradientBrush.GetRectangle(OUT Rect), PathGradientBrush.GetRectangle(Rect*), PathGradientBrush::GetRectangle, PathGradientBrush::GetRectangle(OUT Rect), _gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.GetRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetRectangle(OUT Rect)


## -description


The <b>PathGradientBrush::GetRectangle</b> method gets the smallest rectangle that encloses the boundary path of this path gradient brush.


## -parameters




### -param rect [out]

Type: <b><a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the bounding rectangle. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

