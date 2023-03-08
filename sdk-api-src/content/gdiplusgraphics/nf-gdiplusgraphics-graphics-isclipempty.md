---
UID: NF:gdiplusgraphics.Graphics.IsClipEmpty
title: Graphics::IsClipEmpty (gdiplusgraphics.h)
description: The Graphics::IsClipEmpty method determines whether the clipping region of this Graphics object is empty.
helpviewer_keywords: ["Graphics class [GDI+]","IsClipEmpty method","Graphics.IsClipEmpty","Graphics::IsClipEmpty","IsClipEmpty","IsClipEmpty method [GDI+]","IsClipEmpty method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_IsClipEmpty_","gdiplus._gdiplus_CLASS_Graphics_IsClipEmpty_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsClipEmpty_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\isclipempty.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],IsClipEmpty method, Graphics.IsClipEmpty, Graphics::IsClipEmpty, IsClipEmpty, IsClipEmpty method [GDI+], IsClipEmpty method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsClipEmpty_, gdiplus._gdiplus_CLASS_Graphics_IsClipEmpty_
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
 - Graphics::IsClipEmpty
 - gdiplusgraphics/Graphics::IsClipEmpty
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
 - Graphics.IsClipEmpty
---

# Graphics::IsClipEmpty


## -description

The <b>Graphics::IsClipEmpty</b> method determines whether the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is empty.



## -returns

Type: <b>BOOL</b>

If the clipping region of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

If the clipping region of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is empty, there is no area left in which to draw. Consequently, nothing will be drawn when the clipping region is empty.


#### Examples



The following example determines whether the clipping region is empty and, if it isn't, draws a rectangle.


```cpp
VOID Example_IsClipEmpty(HDC hdc)
{
   Graphics graphics(hdc);

   // If the clipping region is not empty, draw a rectangle.
   if (!graphics.IsClipEmpty())
   {
   graphics.DrawRectangle(&Pen(Color(255, 0, 0, 0), 3), 0, 0, 100, 100);
   }
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclipbounds(outrect)">GetClipBounds Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisibleclipempty">Graphics::IsVisibleClipEmpty</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-resetclip">Graphics::ResetClip</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)">SetClip Methods</a>
