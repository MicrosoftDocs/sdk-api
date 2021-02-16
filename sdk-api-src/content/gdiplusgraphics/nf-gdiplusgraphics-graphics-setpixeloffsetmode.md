---
UID: NF:gdiplusgraphics.Graphics.SetPixelOffsetMode
title: Graphics::SetPixelOffsetMode (gdiplusgraphics.h)
description: The Graphics::SetPixelOffsetMode method sets the pixel offset mode of this Graphics object.
helpviewer_keywords: ["Graphics class [GDI+]","SetPixelOffsetMode method","Graphics.SetPixelOffsetMode","Graphics::SetPixelOffsetMode","SetPixelOffsetMode","SetPixelOffsetMode method [GDI+]","SetPixelOffsetMode method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetPixelOffsetMode_pixelOffsetMode_","gdiplus._gdiplus_CLASS_Graphics_SetPixelOffsetMode_pixelOffsetMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetPixelOffsetMode_pixelOffsetMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setpixeloffsetmode.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetPixelOffsetMode method, Graphics.SetPixelOffsetMode, Graphics::SetPixelOffsetMode, SetPixelOffsetMode, SetPixelOffsetMode method [GDI+], SetPixelOffsetMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetPixelOffsetMode_pixelOffsetMode_, gdiplus._gdiplus_CLASS_Graphics_SetPixelOffsetMode_pixelOffsetMode_
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
 - Graphics::SetPixelOffsetMode
 - gdiplusgraphics/Graphics::SetPixelOffsetMode
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
 - Graphics.SetPixelOffsetMode
---

# Graphics::SetPixelOffsetMode


## -description

The <b>Graphics::SetPixelOffsetMode</b> method sets the pixel offset mode of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param pixelOffsetMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pixeloffsetmode">PixelOffsetMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pixeloffsetmode">PixelOffsetMode</a> enumeration that specifies the pixel offset mode.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pixeloffsetmode">PixelOffsetMode</a>