---
UID: NF:gdiplusgraphics.Graphics.ResetClip
title: Graphics::ResetClip (gdiplusgraphics.h)
description: The Graphics::ResetClip method sets the clipping region of this Graphics object to an infinite region.
helpviewer_keywords: ["Graphics class [GDI+]","ResetClip method","Graphics.ResetClip","Graphics::ResetClip","ResetClip","ResetClip method [GDI+]","ResetClip method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_ResetClip_","gdiplus._gdiplus_CLASS_Graphics_ResetClip_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_ResetClip_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\resetclip.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],ResetClip method, Graphics.ResetClip, Graphics::ResetClip, ResetClip, ResetClip method [GDI+], ResetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ResetClip_, gdiplus._gdiplus_CLASS_Graphics_ResetClip_
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
 - Graphics::ResetClip
 - gdiplusgraphics/Graphics::ResetClip
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
 - Graphics.ResetClip
---

# Graphics::ResetClip


## -description

The <b>Graphics::ResetClip</b> method sets the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to an infinite region.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

If the clipping region of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is infinite, then items drawn by that <b>Graphics</b> object will not be clipped.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and sets its clipping region to a rectangle. The code fills two ellipses that intersect the rectangular clipping region. The first ellipse is clipped, but the second ellipse is not clipped because it is filled after a call to <b>Graphics::ResetClip</b>.


```cpp
VOID Example_ResetClip(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the clipping region, and draw its outline.
   graphics.SetClip(Rect(100, 50, 200, 120));
   Pen blackPen(Color(255, 0, 0, 0), 2.0f);
   graphics.DrawRectangle(&blackPen, 100, 50, 200, 120);

   // Fill a clipped ellipse in red.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&redBrush, 80, 40, 100, 70);

   // Reset the clipping region.
   graphics.ResetClip();

   // Fill an unclipped ellipse with blue.
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&blueBrush, 160, 150, 100, 60);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isclipempty">Graphics::IsClipEmpty</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-intersectclip(inconstrect_)">IntersectClip Methods</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-isempty">IsEmpty</a>
