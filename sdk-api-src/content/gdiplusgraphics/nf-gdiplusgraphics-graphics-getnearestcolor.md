---
UID: NF:gdiplusgraphics.Graphics.GetNearestColor
title: Graphics::GetNearestColor (gdiplusgraphics.h)
description: The Graphics::GetNearestColor method gets the nearest color to the color that is passed in. This method works on 8-bits per pixel or lower display devices for which there is an 8-bit color palette.
helpviewer_keywords: ["GetNearestColor","GetNearestColor method [GDI+]","GetNearestColor method [GDI+]","Graphics class","Graphics class [GDI+]","GetNearestColor method","Graphics.GetNearestColor","Graphics::GetNearestColor","_gdiplus_CLASS_Graphics_GetNearestColor_color_","gdiplus._gdiplus_CLASS_Graphics_GetNearestColor_color_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetNearestColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getnearestcolor.htm
ms.date: 12/05/2018
ms.keywords: GetNearestColor, GetNearestColor method [GDI+], GetNearestColor method [GDI+],Graphics class, Graphics class [GDI+],GetNearestColor method, Graphics.GetNearestColor, Graphics::GetNearestColor, _gdiplus_CLASS_Graphics_GetNearestColor_color_, gdiplus._gdiplus_CLASS_Graphics_GetNearestColor_color_
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
 - Graphics::GetNearestColor
 - gdiplusgraphics/Graphics::GetNearestColor
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
 - Graphics.GetNearestColor
---

# Graphics::GetNearestColor


## -description

The <b>Graphics::GetNearestColor</b> method gets the nearest color to the color that is passed in. This method works on 8-bits per pixel or lower display devices for which there is an 8-bit color palette.

## -parameters

### -param color [in, out]

Type: <b>Color*</b>

Pointer to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that, on input, specifies the color to be tested and, on output, receives the nearest color found in the color palette.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>