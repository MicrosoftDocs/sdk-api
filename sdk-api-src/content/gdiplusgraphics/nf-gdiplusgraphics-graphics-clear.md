---
UID: NF:gdiplusgraphics.Graphics.Clear
title: Graphics::Clear (gdiplusgraphics.h)
description: The Graphics::Clear method clears a Graphicsobject to a specified color.
helpviewer_keywords: ["Clear","Clear method [GDI+]","Clear method [GDI+]","Graphics class","Graphics class [GDI+]","Clear method","Graphics.Clear","Graphics::Clear","_gdiplus_CLASS_Graphics_Clear_color_","gdiplus._gdiplus_CLASS_Graphics_Clear_color_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_Clear_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\clear.htm
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [GDI+], Clear method [GDI+],Graphics class, Graphics class [GDI+],Clear method, Graphics.Clear, Graphics::Clear, _gdiplus_CLASS_Graphics_Clear_color_, gdiplus._gdiplus_CLASS_Graphics_Clear_color_
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
 - Graphics::Clear
 - gdiplusgraphics/Graphics::Clear
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
 - Graphics.Clear
---

# Graphics::Clear


## -description

The <b>Graphics::Clear</b> method clears a 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a specified color.

## -parameters

### -param color [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to the <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color to paint the background.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrect_)">DrawRectangle Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>