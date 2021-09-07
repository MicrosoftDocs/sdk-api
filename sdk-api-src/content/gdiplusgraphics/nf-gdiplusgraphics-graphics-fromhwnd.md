---
UID: NF:gdiplusgraphics.Graphics.FromHWND
title: Graphics::FromHWND (gdiplusgraphics.h)
description: The Graphics::FromHWND method creates a Graphicsobject that is associated with a specified window.
helpviewer_keywords: ["FromHWND","FromHWND method [GDI+]","FromHWND method [GDI+]","Graphics class","Graphics class [GDI+]","FromHWND method","Graphics.FromHWND","Graphics::FromHWND","_gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_","gdiplus._gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\fromhwnd.htm
ms.date: 12/05/2018
ms.keywords: FromHWND, FromHWND method [GDI+], FromHWND method [GDI+],Graphics class, Graphics class [GDI+],FromHWND method, Graphics.FromHWND, Graphics::FromHWND, _gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_, gdiplus._gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_
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
 - Graphics::FromHWND
 - gdiplusgraphics/Graphics::FromHWND
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
 - Graphics.FromHWND
---

# Graphics::FromHWND


## -description

The <b>Graphics::FromHWND</b> method creates a 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that is associated with a specified window.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

Handle to the window that will be associated with the new 
					<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

### -param icm [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object applies color adjustment according to the ICC profile associated with the display device. <b>TRUE</b> specifies that color adjustment is applied, and <b>FALSE</b> specifies that color adjustment is not applied. The default value is <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)">FromHDC Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromimage">Graphics::FromImage</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">Graphics::GetHDC</a>