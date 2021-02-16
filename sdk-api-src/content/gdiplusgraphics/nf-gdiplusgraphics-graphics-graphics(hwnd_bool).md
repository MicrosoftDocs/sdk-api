---
UID: NF:gdiplusgraphics.Graphics.Graphics(HWND,BOOL)
title: Graphics::Graphics(IN HWND,IN BOOL) (gdiplusgraphics.h)
description: Creates a Graphics::Graphics object that is associated with a specified window.
helpviewer_keywords: ["Graphics","Graphics class [GDI+]","Graphics constructor","Graphics constructor [GDI+]","Graphics constructor [GDI+]","Graphics class","Graphics.Graphics","Graphics.Graphics(HWND","BOOL)","Graphics.Graphics(IN HWND","IN BOOL)","Graphics::Graphics","Graphics::Graphics(IN HWND","IN BOOL)","_gdiplus_CLASS_Graphics_Graphics_hwnd_icm_","gdiplus._gdiplus_CLASS_Graphics_Graphics_hwnd_icm_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_Graphics_hwnd_icm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsconstructors\graphics_7hwnd_icm.htm
ms.date: 12/05/2018
ms.keywords: Graphics, Graphics class [GDI+],Graphics constructor, Graphics constructor [GDI+], Graphics constructor [GDI+],Graphics class, Graphics.Graphics, Graphics.Graphics(HWND,BOOL), Graphics.Graphics(IN HWND,IN BOOL), Graphics::Graphics, Graphics::Graphics(IN HWND,IN BOOL), _gdiplus_CLASS_Graphics_Graphics_hwnd_icm_, gdiplus._gdiplus_CLASS_Graphics_Graphics_hwnd_icm_
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
 - Graphics::Graphics
 - gdiplusgraphics/Graphics::Graphics
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
 - Graphics.Graphics
---

# Graphics::Graphics(IN HWND,IN BOOL)


## -description

Creates a <b>Graphics::Graphics</b> object that is associated with a specified window.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

Handle to a window that will be associated with the new <b>Graphics::Graphics</b> object.

### -param icm [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new <b>Graphics::Graphics</b> object applies color adjustment according to the ICC profile associated with the display device. <b>TRUE</b> specifies that color adjustment is applied, and <b>FALSE</b> specifies that color adjustment is not applied. The default value is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/gdiplus/-gdiplus-getting-started-use">Getting Started</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>