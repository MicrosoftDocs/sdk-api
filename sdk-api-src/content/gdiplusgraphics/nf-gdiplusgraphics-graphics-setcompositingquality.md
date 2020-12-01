---
UID: NF:gdiplusgraphics.Graphics.SetCompositingQuality
title: Graphics::SetCompositingQuality (gdiplusgraphics.h)
description: The Graphics::SetCompositingQuality method sets the compositing quality of this Graphics object.
helpviewer_keywords: ["Graphics class [GDI+]","SetCompositingQuality method","Graphics.SetCompositingQuality","Graphics::SetCompositingQuality","SetCompositingQuality","SetCompositingQuality method [GDI+]","SetCompositingQuality method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetCompositingQuality_compositingQuality_","gdiplus._gdiplus_CLASS_Graphics_SetCompositingQuality_compositingQuality_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetCompositingQuality_compositingQuality_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setcompositingquality.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetCompositingQuality method, Graphics.SetCompositingQuality, Graphics::SetCompositingQuality, SetCompositingQuality, SetCompositingQuality method [GDI+], SetCompositingQuality method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetCompositingQuality_compositingQuality_, gdiplus._gdiplus_CLASS_Graphics_SetCompositingQuality_compositingQuality_
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
 - Graphics::SetCompositingQuality
 - gdiplusgraphics/Graphics::SetCompositingQuality
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
 - Graphics.SetCompositingQuality
---

# Graphics::SetCompositingQuality


## -description

The <b>Graphics::SetCompositingQuality</b> method sets the compositing quality of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param compositingQuality [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingquality">CompositingQuality</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingquality">CompositingQuality</a> enumeration that specifies the compositing quality.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-alpha-blending-lines-and-fills-use">Alpha Blending Lines and Fills</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingmode">Graphics::GetCompositingMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingquality">Graphics::GetCompositingQuality</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode">Graphics::SetCompositingMode</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-new-features-about">New Features</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>