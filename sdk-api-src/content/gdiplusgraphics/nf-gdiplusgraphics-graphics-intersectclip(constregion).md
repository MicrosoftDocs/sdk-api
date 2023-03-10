---
UID: NF:gdiplusgraphics.Graphics.IntersectClip(constRegion)
title: Graphics::IntersectClip(IN const Region) (gdiplusgraphics.h)
description: The Graphics::IntersectClip method updates the clipping region of this Graphics object to the portion of the specified region that intersects with the current clipping region of this Graphics object.
helpviewer_keywords: ["Graphics class [GDI+]","IntersectClip method","Graphics.IntersectClip","Graphics.IntersectClip(IN const Region)","Graphics.IntersectClip(const Region*)","Graphics::IntersectClip","Graphics::IntersectClip(IN const Region)","IntersectClip","IntersectClip method [GDI+]","IntersectClip method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_IntersectClip_region_","gdiplus._gdiplus_CLASS_Graphics_IntersectClip_region_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_IntersectClip_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsintersectclipmethods\intersectclip_28region.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],IntersectClip method, Graphics.IntersectClip, Graphics.IntersectClip(IN const Region), Graphics.IntersectClip(const Region*), Graphics::IntersectClip, Graphics::IntersectClip(IN const Region), IntersectClip, IntersectClip method [GDI+], IntersectClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IntersectClip_region_, gdiplus._gdiplus_CLASS_Graphics_IntersectClip_region_
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
 - Graphics::IntersectClip
 - gdiplusgraphics/Graphics::IntersectClip
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
 - Graphics.IntersectClip
---

# Graphics::IntersectClip(IN const Region)


## -description

The <b>Graphics::IntersectClip</b> method updates the clipping region of this 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to the portion of the specified region that intersects with the current clipping region of this 
			<b>Graphics</b> object.

## -parameters

### -param region [in]

Type: <b>const Region*</b>

Pointer to a region that is used to update the clipping region of this 
					<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclipbounds(outrect)">GetClipBounds Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)">SetClip Methods</a>