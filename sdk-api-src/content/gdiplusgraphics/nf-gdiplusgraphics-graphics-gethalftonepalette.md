---
UID: NF:gdiplusgraphics.Graphics.GetHalftonePalette
title: Graphics::GetHalftonePalette (gdiplusgraphics.h)
description: The Graphics::GetHalftonePalette method gets a Windows halftone palette.
helpviewer_keywords: ["GetHalftonePalette","GetHalftonePalette method [GDI+]","GetHalftonePalette method [GDI+]","Graphics class","Graphics class [GDI+]","GetHalftonePalette method","Graphics.GetHalftonePalette","Graphics::GetHalftonePalette","_gdiplus_CLASS_Graphics_GetHalftonePalette_","gdiplus._gdiplus_CLASS_Graphics_GetHalftonePalette_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetHalftonePalette_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\gethalftonepalette.htm
ms.date: 12/05/2018
ms.keywords: GetHalftonePalette, GetHalftonePalette method [GDI+], GetHalftonePalette method [GDI+],Graphics class, Graphics class [GDI+],GetHalftonePalette method, Graphics.GetHalftonePalette, Graphics::GetHalftonePalette, _gdiplus_CLASS_Graphics_GetHalftonePalette_, gdiplus._gdiplus_CLASS_Graphics_GetHalftonePalette_
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
 - Graphics::GetHalftonePalette
 - gdiplusgraphics/Graphics::GetHalftonePalette
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
 - Graphics.GetHalftonePalette
---

# Graphics::GetHalftonePalette


## -description

The <b>Graphics::GetHalftonePalette</b> method gets a Windows halftone palette.



## -returns

Type: <b>static</b>

This method returns a handle to a Windows halftone palette.

## -remarks

The purpose of the <b>Graphics::GetHalftonePalette</b> method is to enable GDI+ to produce a better quality halftone when the display uses 8 bits per pixel. To display an image using the halftone palette, use the following procedure: 

<ol>
<li>Call <b>Graphics::GetHalftonePalette</b> to get a GDI+ halftone palette. </li>
<li>Select the halftone palette into a device context. </li>
<li>Realize the palette by calling the 
						<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a> function. </li>
<li>Construct a 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object from a handle to the device context. </li>
<li>Call the
<a href="/previous-versions/ms536028(v=vs.85)">Graphics::DrawImage</a> method of the 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. </li>
</ol>
Be sure to delete the palette when you have finished using it. If you do not follow the preceding procedure, then on an 8-bits-per-pixel-display device, the default, 16-color process is used, which results in a lesser quality halftone.


#### Examples



The following example draws the same image twice. Before the image is drawn the second time, the code gets a halftone palette, selects the palette into a device context, and realizes the palette.


```cpp
VOID Example_GetHalftonePalette(HDC hdc)
{
   Image image(L"Mosaic.png");
   
   Graphics* graphics1 = new Graphics(hdc);
   graphics1->DrawImage(&image, 10, 10);
   delete graphics1;
   
   HPALETTE hPalette = Graphics::GetHalftonePalette();
   SelectPalette(hdc, hPalette, FALSE);
   RealizePalette(hdc);
   Graphics* graphics2 = new Graphics(hdc);
   graphics2->DrawImage(&image, 300, 10);
   delete graphics2;
   DeleteObject(hPalette);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpalette">GetPalette</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpalette"> SetPalette</a>
