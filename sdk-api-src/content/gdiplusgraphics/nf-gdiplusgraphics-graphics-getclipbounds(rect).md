---
UID: NF:gdiplusgraphics.Graphics.GetClipBounds(Rect)
title: Graphics::GetClipBounds(OUT Rect) (gdiplusgraphics.h)
description: The Graphics::GetClipBounds method gets a rectangle that encloses the clipping region of this Graphics object. (overload 1/2)
helpviewer_keywords: ["GetClipBounds","GetClipBounds method [GDI+]","GetClipBounds method [GDI+]","Graphics class","Graphics class [GDI+]","GetClipBounds method","Graphics.GetClipBounds","Graphics.GetClipBounds(OUT Rect)","Graphics.GetClipBounds(Rect*)","Graphics::GetClipBounds","Graphics::GetClipBounds(OUT Rect)","_gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_","gdiplus._gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsgetclipboundsmethods\getclipbounds.htm
ms.date: 12/05/2018
ms.keywords: GetClipBounds, GetClipBounds method [GDI+], GetClipBounds method [GDI+],Graphics class, Graphics class [GDI+],GetClipBounds method, Graphics.GetClipBounds, Graphics.GetClipBounds(OUT Rect), Graphics.GetClipBounds(Rect*), Graphics::GetClipBounds, Graphics::GetClipBounds(OUT Rect), _gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_
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
 - Graphics::GetClipBounds
 - gdiplusgraphics/Graphics::GetClipBounds
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
 - Graphics.GetClipBounds
---

# Graphics::GetClipBounds(OUT Rect)


## -description

The <b>Graphics::GetClipBounds</b> method gets a rectangle that encloses the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param rect [out]

Type: <b>Rect*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the rectangle that encloses the clipping region.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The world transformation is applied to the clipping region and then the enclosing rectangle is calculated.

If you do not explicitly set the clipping region of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, its clipping region is infinite. When the clipping region is infinite, <b>Graphics::GetClipBounds</b> returns a large rectangle. The 
				<b>X</b> and 
				<b>Y</b> data members of that rectangle are large negative numbers, and the 
				<b>Width</b> and 
				<b>Height</b> data members are large positive numbers.


#### Examples



The following example sets a clipping region, gets the rectangle that encloses the clipping region, and then fills the rectangle.


```cpp
VOID Example_GetClipBounds(HDC hdc)
{
   Graphics graphics(hdc);

   Region   myRegion(Rect(25, 25, 100, 50));
   Rect     rect(40, 60, 100, 50);
   Region   gRegion;
   Rect     enclosingRect;

   SolidBrush  blueBrush(Color(100, 0, 0, 255));
   Pen         greenPen(Color(255, 0, 255, 0), 1.5f);

   // Modify the region by using a rectangle.
   myRegion.Union(rect);

   // Set the clipping region of the graphics object.
   graphics.SetClip(&myRegion);

   // Now, get the clipping region, and fill it.
   graphics.GetClip(&gRegion);
   graphics.FillRegion(&blueBrush, &gRegion);

   // Get a rectangle that encloses the clipping region, and draw the enclosing
   // rectangle.
   graphics.GetClipBounds(&enclosingRect);
   graphics.ResetClip();
   graphics.DrawRectangle(&greenPen, enclosingRect);}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getvisibleclipbounds(outrect)">GetVisibleClipBounds Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)">SetClip Methods</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
