---
UID: NF:gdiplusgraphics.Graphics.SetClip(HRGN,CombineMode)
title: Graphics::SetClip(IN HRGN,IN CombineMode) (gdiplusgraphics.h)
description: The Graphics::SetClip method updates the clipping region of this Graphics object to a region that is the combination of itself and a Windows Graphics Device Interface (GDI) region.
helpviewer_keywords: ["Graphics class [GDI+]","SetClip method","Graphics.SetClip","Graphics.SetClip(HRGN","CombineMode)","Graphics.SetClip(IN HRGN","IN CombineMode)","Graphics::SetClip","Graphics::SetClip(IN HRGN","IN CombineMode)","SetClip","SetClip method [GDI+]","SetClip method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_","gdiplus._gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicssetclipmethods\setclip_93hrgn_combinemode.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetClip method, Graphics.SetClip, Graphics.SetClip(HRGN,CombineMode), Graphics.SetClip(IN HRGN,IN CombineMode), Graphics::SetClip, Graphics::SetClip(IN HRGN,IN CombineMode), SetClip, SetClip method [GDI+], SetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_, gdiplus._gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_
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
 - Graphics::SetClip
 - gdiplusgraphics/Graphics::SetClip
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
 - Graphics.SetClip
---

# Graphics::SetClip(IN HRGN,IN CombineMode)


## -description

The <b>Graphics::SetClip</b> method updates the clipping region of this  <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a region that is the combination of itself and a Windows Graphics Device Interface (GDI) region.

## -parameters

### -param hRgn [in]

Type: <b>HRGN</b>

Handle to a GDI region to be combined with the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. This is provided for legacy code. New applications should pass a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object as the first parameter.

### -param combineMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-combinemode">CombineMode</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-combinemode">CombineMode</a> enumeration that specifies how the GDI region is combined with the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The default value is CombineModeReplace.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

This method assumes that the GDI region specified by 
				<i>hRgn</i> is already in device units, so it does not transform the coordinates of the GDI region.


#### Examples



The following example uses a GDI region to update the clipping region.


```cpp
VOID Example_SetClip2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Region object, and get its handle.
   Region region(Rect(0, 0, 100, 100));
   HRGN hRegion = region.GetHRGN(&graphics);

   // Set the clipping region with hRegion.
   graphics.SetClip(hRegion);

   // Fill a rectangle to demonstrate the clipping region.
   graphics.FillRectangle(&SolidBrush(Color(255, 0, 0, 0)), 0, 0, 500, 500);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-combinemode">CombineMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclipbounds(outrect)">GetClipBounds Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isclipempty">Graphics::IsClipEmpty</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-resetclip">Graphics::ResetClip</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-intersectclip(inconstrect_)">IntersectClip Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-translateclip(inint_inint)">TranslateClip Methods</a>