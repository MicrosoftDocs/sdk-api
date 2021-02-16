---
UID: NF:gdiplusgraphics.Graphics.SetPageScale
title: Graphics::SetPageScale (gdiplusgraphics.h)
description: The Graphics::SetPageScale method sets the scaling factor for the page transformation of this Graphics object. The page transformation converts page coordinates to device coordinates.
helpviewer_keywords: ["Graphics class [GDI+]","SetPageScale method","Graphics.SetPageScale","Graphics::SetPageScale","SetPageScale","SetPageScale method [GDI+]","SetPageScale method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetPageScale_scale_","gdiplus._gdiplus_CLASS_Graphics_SetPageScale_scale_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetPageScale_scale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setpagescale.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetPageScale method, Graphics.SetPageScale, Graphics::SetPageScale, SetPageScale, SetPageScale method [GDI+], SetPageScale method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetPageScale_scale_, gdiplus._gdiplus_CLASS_Graphics_SetPageScale_scale_
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
 - Graphics::SetPageScale
 - gdiplusgraphics/Graphics::SetPageScale
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
 - Graphics.SetPageScale
---

# Graphics::SetPageScale


## -description

The <b>Graphics::SetPageScale</b> method sets the scaling factor for the page transformation of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The page transformation converts page coordinates to device coordinates.

## -parameters

### -param scale [in]

Type: <b>REAL</b>

Real number that specifies the scaling factor.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix">Graphics::GetDpiX</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy">Graphics::GetDpiY</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale">Graphics::GetPageScale</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit">Graphics::GetPageUnit</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit">Graphics::SetPageUnit</a>



<a href="/windows/desktop/gdiplus/-gdiplus-types-of-coordinate-systems-about">Types of Coordinate Systems</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>