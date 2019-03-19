---
UID: NF:gdipluspath.PathGradientBrush.GetRectangle(OUT Rect)
title: PathGradientBrush::GetRectangle(OUT Rect) (gdipluspath.h)
author: windows-sdk-content
description: The PathGradientBrush::GetRectangle method gets the smallest rectangle that encloses the boundary path of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushgetrectanglemethods\getrectangle_89rectrect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRectangle, GetRectangle method [GDI+], GetRectangle method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetRectangle method, PathGradientBrush.GetRectangle, PathGradientBrush.GetRectangle(OUT Rect), PathGradientBrush.GetRectangle(Rect*), PathGradientBrush::GetRectangle, PathGradientBrush::GetRectangle(OUT Rect), _gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a> object that receives the bounding rectangle. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>
 

 

