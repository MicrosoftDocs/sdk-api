---
UID: NF:gdiplusgraphics.Graphics.GetVisibleClipBounds(Rect)
title: Graphics::GetVisibleClipBounds(OUT Rect) (gdiplusgraphics.h)
description: The Graphics::GetVisibleClipBounds method gets a rectangle that encloses the visible clipping region of this Graphics object. (overload 1/2)
helpviewer_keywords: ["GetVisibleClipBounds","GetVisibleClipBounds method [GDI+]","GetVisibleClipBounds method [GDI+]","Graphics class","Graphics class [GDI+]","GetVisibleClipBounds method","Graphics.GetVisibleClipBounds","Graphics.GetVisibleClipBounds(OUT Rect)","Graphics.GetVisibleClipBounds(Rect*)","Graphics::GetVisibleClipBounds","Graphics::GetVisibleClipBounds(OUT Rect)","_gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_","gdiplus._gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsgetvisibleclipboundsmethods\getvisibleclipbounds.htm
ms.date: 12/05/2018
ms.keywords: GetVisibleClipBounds, GetVisibleClipBounds method [GDI+], GetVisibleClipBounds method [GDI+],Graphics class, Graphics class [GDI+],GetVisibleClipBounds method, Graphics.GetVisibleClipBounds, Graphics.GetVisibleClipBounds(OUT Rect), Graphics.GetVisibleClipBounds(Rect*), Graphics::GetVisibleClipBounds, Graphics::GetVisibleClipBounds(OUT Rect), _gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_
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
 - Graphics::GetVisibleClipBounds
 - gdiplusgraphics/Graphics::GetVisibleClipBounds
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
 - Graphics.GetVisibleClipBounds
---

# Graphics::GetVisibleClipBounds(OUT Rect)


## -description

The <b>Graphics::GetVisibleClipBounds</b> method gets a rectangle that encloses the visible clipping region of this 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this 
			<b>Graphics</b> object and the clipping region of the window.

## -parameters

### -param rect [out]

Type: <b>Rect*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the rectangle that encloses the visible clipping region.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclipbounds(outrect)">GetClipBounds Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisibleclipempty">Graphics::IsVisibleClipEmpty</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisible(inconstpointf_)">IsVisible Methods</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
