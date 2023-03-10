---
UID: NF:gdipluspath.PathGradientBrush.GetRectangle(Rect)
title: PathGradientBrush::GetRectangle(OUT Rect) (gdipluspath.h)
description: The PathGradientBrush::GetRectangle method gets the smallest rectangle that encloses the boundary path of this path gradient brush. (overload 1/2)
helpviewer_keywords: ["GetRectangle","GetRectangle method [GDI+]","GetRectangle method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetRectangle method","PathGradientBrush.GetRectangle","PathGradientBrush.GetRectangle(OUT Rect)","PathGradientBrush.GetRectangle(Rect*)","PathGradientBrush::GetRectangle","PathGradientBrush::GetRectangle(OUT Rect)","_gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushgetrectanglemethods\getrectangle_89rectrect.htm
ms.date: 12/05/2018
ms.keywords: GetRectangle, GetRectangle method [GDI+], GetRectangle method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetRectangle method, PathGradientBrush.GetRectangle, PathGradientBrush.GetRectangle(OUT Rect), PathGradientBrush.GetRectangle(Rect*), PathGradientBrush::GetRectangle, PathGradientBrush::GetRectangle(OUT Rect), _gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetRectangle_Rect_rect_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathGradientBrush::GetRectangle
 - gdipluspath/PathGradientBrush::GetRectangle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.GetRectangle
---

# PathGradientBrush::GetRectangle(OUT Rect)


## -description

The <b>PathGradientBrush::GetRectangle</b> method gets the smallest rectangle that encloses the boundary path of this path gradient brush.

## -parameters

### -param rect [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the bounding rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
