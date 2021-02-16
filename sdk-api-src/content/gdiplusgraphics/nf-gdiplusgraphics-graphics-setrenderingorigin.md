---
UID: NF:gdiplusgraphics.Graphics.SetRenderingOrigin
title: Graphics::SetRenderingOrigin (gdiplusgraphics.h)
description: The Graphics::SetRenderingOrigin method sets the rendering origin of this Graphics object. The rendering origin is used to set the dither origin for 8-bits-per-pixel and 16-bits-per-pixel dithering and is also used to set the origin for hatch brushes.
helpviewer_keywords: ["Graphics class [GDI+]","SetRenderingOrigin method","Graphics.SetRenderingOrigin","Graphics::SetRenderingOrigin","SetRenderingOrigin","SetRenderingOrigin method [GDI+]","SetRenderingOrigin method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_","gdiplus._gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setrenderingorigin.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetRenderingOrigin method, Graphics.SetRenderingOrigin, Graphics::SetRenderingOrigin, SetRenderingOrigin, SetRenderingOrigin method [GDI+], SetRenderingOrigin method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_, gdiplus._gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_
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
 - Graphics::SetRenderingOrigin
 - gdiplusgraphics/Graphics::SetRenderingOrigin
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
 - Graphics.SetRenderingOrigin
---

# Graphics::SetRenderingOrigin


## -description

The <b>Graphics::SetRenderingOrigin</b> method sets the rendering origin of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The rendering origin is used to set the dither origin for 8-bits-per-pixel and 16-bits-per-pixel dithering and is also used to set the origin for hatch brushes.

## -parameters

### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the rendering origin.

### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the rendering origin.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getrenderingorigin">Graphics::GetRenderingOrigin</a>