---
UID: NF:gdiplusgraphics.Graphics.ReleaseHDC
title: Graphics::ReleaseHDC (gdiplusgraphics.h)
description: The Graphics::ReleaseHDC method releases a device context handle obtained by a previous call to the Graphics::GetHDC method of this Graphics object.
helpviewer_keywords: ["Graphics class [GDI+]","ReleaseHDC method","Graphics.ReleaseHDC","Graphics::ReleaseHDC","ReleaseHDC","ReleaseHDC method [GDI+]","ReleaseHDC method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_ReleaseHDC_hdc_","gdiplus._gdiplus_CLASS_Graphics_ReleaseHDC_hdc_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_ReleaseHDC_hdc_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\releasehdc.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],ReleaseHDC method, Graphics.ReleaseHDC, Graphics::ReleaseHDC, ReleaseHDC, ReleaseHDC method [GDI+], ReleaseHDC method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ReleaseHDC_hdc_, gdiplus._gdiplus_CLASS_Graphics_ReleaseHDC_hdc_
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
 - Graphics::ReleaseHDC
 - gdiplusgraphics/Graphics::ReleaseHDC
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
 - Graphics.ReleaseHDC
---

# Graphics::ReleaseHDC


## -description

The <b>Graphics::ReleaseHDC</b> method releases a device context handle obtained by a previous call to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">Graphics::GetHDC</a> method of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

Handle to a device context obtained by a previous call to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">Graphics::GetHDC</a> method of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)">FromHDC Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">Graphics::GetHDC</a>