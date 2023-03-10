---
UID: NF:gdiplusgraphics.Graphics.DrawPolygon(constPen,constPoint,INT)
title: Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawPolygon method draws a polygon. (overload 2/2)
helpviewer_keywords: ["DrawPolygon","DrawPolygon method [GDI+]","DrawPolygon method [GDI+]","Graphics class","Graphics class [GDI+]","DrawPolygon method","Graphics.DrawPolygon","Graphics.DrawPolygon(IN const Pen","IN const Point","IN INT)","Graphics.DrawPolygon(const Pen*","const Point*","INT*)","Graphics::DrawPolygon","Graphics::DrawPolygon(IN const Pen","IN const Point","IN INT)","_gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_Point_points_INT_count_","gdiplus._gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_Point_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawpolygonmethods\drawpolygon.htm
ms.date: 12/05/2018
ms.keywords: DrawPolygon, DrawPolygon method [GDI+], DrawPolygon method [GDI+],Graphics class, Graphics class [GDI+],DrawPolygon method, Graphics.DrawPolygon, Graphics.DrawPolygon(IN const Pen,IN const Point,IN INT), Graphics.DrawPolygon(const Pen*,const Point*,INT*), Graphics::DrawPolygon, Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_Point_points_INT_count_
req.header: gdiplusgraphics.h
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
 - Graphics::DrawPolygon
 - gdiplusgraphics/Graphics::DrawPolygon
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
 - Graphics.DrawPolygon
---

# Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT)


## -description

The <b>Graphics::DrawPolygon</b> method draws a polygon.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the polygon.

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that specify the vertices of the polygon.

### -param count [in]

Type: <b>INT*</b>

Integer that specifies the number of elements in the 
					<i>points</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

If the first and last coordinates in the 
				<i>points</i> array are not identical, a line is drawn between them to close the polygon.


#### Examples



The following example draws a polygon, defined by an array of points.


```cpp
VOID Example_DrawPolygon(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Create an array of Point objects that define the polygon.
   Point point1(100, 100);
   Point point2(200, 130);
   Point point3(150, 200);
   Point point4(50, 200);
   Point point5(0, 130);
   Point points[5] = {point1, point2, point3, point4, point5};
   Point* pPoints = points;

   // Draw the polygon.
   graphics.DrawPolygon(&blackPen, pPoints, 5);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpointf_inint_infillmode)">FillPolygon Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/gdiplus/-gdiplus-polygons-about">Polygons</a>
