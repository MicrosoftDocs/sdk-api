---
UID: NF:gdiplusgraphics.Graphics.IsVisibleClipEmpty
title: Graphics::IsVisibleClipEmpty (gdiplusgraphics.h)
description: The Graphics::IsVisibleClipEmpty method determines whether the visible clipping region of this Graphics object is empty. The visible clipping region is the intersection of the clipping region of this Graphics object and the clipping region of the window.
helpviewer_keywords: ["Graphics class [GDI+]","IsVisibleClipEmpty method","Graphics.IsVisibleClipEmpty","Graphics::IsVisibleClipEmpty","IsVisibleClipEmpty","IsVisibleClipEmpty method [GDI+]","IsVisibleClipEmpty method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_IsVisibleClipEmpty_","gdiplus._gdiplus_CLASS_Graphics_IsVisibleClipEmpty_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsVisibleClipEmpty_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\isvisibleclipempty.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],IsVisibleClipEmpty method, Graphics.IsVisibleClipEmpty, Graphics::IsVisibleClipEmpty, IsVisibleClipEmpty, IsVisibleClipEmpty method [GDI+], IsVisibleClipEmpty method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsVisibleClipEmpty_, gdiplus._gdiplus_CLASS_Graphics_IsVisibleClipEmpty_
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
 - Graphics::IsVisibleClipEmpty
 - gdiplusgraphics/Graphics::IsVisibleClipEmpty
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
 - Graphics.IsVisibleClipEmpty
---

# Graphics::IsVisibleClipEmpty


## -description

The <b>Graphics::IsVisibleClipEmpty</b> method determines whether the visible clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is empty. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.



## -returns

Type: <b>BOOL</b>

If the visible clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

If the visible clipping region of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is empty, there is no area left in which to draw. Consequently, nothing will be drawn when the visible clipping region is empty.


#### Examples



The following example determines whether the visible clipping region is empty. If it is not empty, it draws a rectangle.


```cpp
VOID Example_IsVisibleClipEmpty(HDC hdc)
{
   Graphics graphics(hdc);

   // If the clipping region is not empty, draw a rectangle.
   if (!graphics.IsVisibleClipEmpty())
   {
   graphics.DrawRectangle(&Pen(Color(255, 0, 0, 0), 3), 0, 0, 100, 100);
   }
}
```
