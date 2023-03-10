---
UID: NF:gdiplusgraphics.Graphics.ExcludeClip(constRect&)
title: Graphics::ExcludeClip(IN const Rect &) (gdiplusgraphics.h)
description: The Graphics::ExcludeClip method updates the clipping region to the portion of itself that does not intersect the specified rectangle. (overload 2/2)
helpviewer_keywords: ["ExcludeClip","ExcludeClip method [GDI+]","ExcludeClip method [GDI+]","Graphics class","Graphics class [GDI+]","ExcludeClip method","Graphics.ExcludeClip","Graphics.ExcludeClip(IN const Rect &)","Graphics.ExcludeClip(const Rect&)","Graphics::ExcludeClip","Graphics::ExcludeClip(IN const Rect &)","_gdiplus_CLASS_Graphics_ExcludeClip_Rect_rect_","gdiplus._gdiplus_CLASS_Graphics_ExcludeClip_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_ExcludeClip_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsexcludeclipmethods\excludeclip.htm
ms.date: 12/05/2018
ms.keywords: ExcludeClip, ExcludeClip method [GDI+], ExcludeClip method [GDI+],Graphics class, Graphics class [GDI+],ExcludeClip method, Graphics.ExcludeClip, Graphics.ExcludeClip(IN const Rect &), Graphics.ExcludeClip(const Rect&), Graphics::ExcludeClip, Graphics::ExcludeClip(IN const Rect &), _gdiplus_CLASS_Graphics_ExcludeClip_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_ExcludeClip_Rect_rect_
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
 - Graphics::ExcludeClip
 - gdiplusgraphics/Graphics::ExcludeClip
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
 - Graphics.ExcludeClip
---

# Graphics::ExcludeClip(IN const Rect &)


## -description

The <b>Graphics::ExcludeClip</b> method updates the clipping region to the portion of itself that does not intersect the specified rectangle.

## -parameters

### -param rect [in]

Type: <b>const Rect&amp;</b>

Reference to a rectangle to use to update the clipping region.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
