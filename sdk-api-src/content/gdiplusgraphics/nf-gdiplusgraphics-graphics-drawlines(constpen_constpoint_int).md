---
UID: NF:gdiplusgraphics.Graphics.DrawLines(constPen,constPoint,INT)
title: Graphics::DrawLines(IN const Pen,IN const Point,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawLines method draws a sequence of connected lines. (overload 2/2)
helpviewer_keywords: ["DrawLines","DrawLines method [GDI+]","DrawLines method [GDI+]","Graphics class","Graphics class [GDI+]","DrawLines method","Graphics.DrawLines","Graphics.DrawLines(IN const Pen","IN const Point","IN INT)","Graphics.DrawLines(const Pen*","const Point*","INT)","Graphics::DrawLines","Graphics::DrawLines(IN const Pen","IN const Point","IN INT)","_gdiplus_CLASS_Graphics_DrawLines_Pen_pen_Point_points_INT_count_","gdiplus._gdiplus_CLASS_Graphics_DrawLines_Pen_pen_Point_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawLines_Pen_pen_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawlinesmethods\drawlines.htm
ms.date: 12/05/2018
ms.keywords: DrawLines, DrawLines method [GDI+], DrawLines method [GDI+],Graphics class, Graphics class [GDI+],DrawLines method, Graphics.DrawLines, Graphics.DrawLines(IN const Pen,IN const Point,IN INT), Graphics.DrawLines(const Pen*,const Point*,INT), Graphics::DrawLines, Graphics::DrawLines(IN const Pen,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawLines_Pen_pen_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawLines_Pen_pen_Point_points_INT_count_
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
 - Graphics::DrawLines
 - gdiplusgraphics/Graphics::DrawLines
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
 - Graphics.DrawLines
---

# Graphics::DrawLines(IN const Pen,IN const Point,IN INT)


## -description

The <b>Graphics::DrawLines</b> method draws a sequence of connected lines.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the lines.

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that specify the starting and ending points of the lines.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.

## -remarks

Each line requires a starting point and an ending point. The ending point of each line is the starting point for the next. 


#### Examples



The following example draws a sequence of connected lines.


```cpp

VOID Example_DrawLines(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Create an array of Point objects that define the lines to draw.
   Point point1(10, 10);
   Point point2(10, 100);
   Point point3(200, 50);
   Point point4(250, 300);

   Point points[4] = {point1, point2, point3, point4};
   Point* pPoints = points;

   // Draw the lines.
   graphics.DrawLines(&blackPen, pPoints, 4);
}

```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpointf__inconstpointf_)">DrawLine Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
