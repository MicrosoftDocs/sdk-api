---
UID: NF:gdipluspath.GraphicsPath.Reverse
title: GraphicsPath::Reverse (gdipluspath.h)
description: The GraphicsPath::Reverse method reverses the order of the points that define this path's lines and curves.
helpviewer_keywords: ["GraphicsPath class [GDI+]","Reverse method","GraphicsPath.Reverse","GraphicsPath::Reverse","Reverse","Reverse method [GDI+]","Reverse method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_Reverse_","gdiplus._gdiplus_CLASS_GraphicsPath_Reverse_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Reverse_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\reverse.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],Reverse method, GraphicsPath.Reverse, GraphicsPath::Reverse, Reverse, Reverse method [GDI+], Reverse method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Reverse_, gdiplus._gdiplus_CLASS_GraphicsPath_Reverse_
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
 - GraphicsPath::Reverse
 - gdipluspath/GraphicsPath::Reverse
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
 - GraphicsPath.Reverse
---

# GraphicsPath::Reverse


## -description

The <b>GraphicsPath::Reverse</b> method reverses the order of the points that define this path's lines and curves.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration. 

This method reverses the order of the elements in the array of points and in the array of types.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object <i>path</i>, adds two lines to <i>path</i>, calls the <b>Reverse</b> method, and then draws <i>path</i>.


```cpp

VOID ReverseExample(HDC hdc)
{
   Graphics graphics(hdc);
   GraphicsPath path;

   // Set up and call Reverse.
   Point pts[] = {Point(10, 60),
                  Point(50, 110),
                  Point(90, 60)};
   path.AddLines(pts, 3);
   path.Reverse();

   // Draw the path.
   graphics.DrawPath(&Pen(Color(128, 255, 0, 0), 2), &path);
}
 
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)">AddLines Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
