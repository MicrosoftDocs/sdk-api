---
UID: NF:gdiplusgraphics.Graphics.TranslateClip(INT,INT)
title: Graphics::TranslateClip(IN INT,IN INT) (gdiplusgraphics.h)
description: The Graphics::TranslateClip method translates the clipping region of this Graphics object. (overload 2/2)
helpviewer_keywords: ["Graphics class [GDI+]","TranslateClip method","Graphics.TranslateClip","Graphics.TranslateClip(IN INT","IN INT)","Graphics.TranslateClip(INT","INT)","Graphics::TranslateClip","Graphics::TranslateClip(IN INT","IN INT)","TranslateClip","TranslateClip method [GDI+]","TranslateClip method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_","gdiplus._gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicstranslateclipmethods\translateclip.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],TranslateClip method, Graphics.TranslateClip, Graphics.TranslateClip(IN INT,IN INT), Graphics.TranslateClip(INT,INT), Graphics::TranslateClip, Graphics::TranslateClip(IN INT,IN INT), TranslateClip, TranslateClip method [GDI+], TranslateClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_, gdiplus._gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_
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
 - Graphics::TranslateClip
 - gdiplusgraphics/Graphics::TranslateClip
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
 - Graphics.TranslateClip
---

# Graphics::TranslateClip(IN INT,IN INT)


## -description

The <b>Graphics::TranslateClip</b> method translates the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param dx [in]

Type: <b>INT</b>

Integer that specifies the horizontal component of the translation.

### -param dy [in]

Type: <b>INT</b>

Integer that specifies the vertical component of the translation.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isclipempty">Graphics::IsClipEmpty</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-intersectclip(inconstrect_)">IntersectClip Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)">SetClip Methods</a>
