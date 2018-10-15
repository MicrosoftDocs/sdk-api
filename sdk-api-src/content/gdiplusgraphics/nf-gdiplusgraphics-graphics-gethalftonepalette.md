---
UID: NF:gdiplusgraphics.Graphics.GetHalftonePalette
title: Graphics::GetHalftonePalette
author: windows-sdk-content
description: The Graphics::GetHalftonePalette method gets a Windows halftone palette.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetHalftonePalette_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\gethalftonepalette.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetHalftonePalette, GetHalftonePalette method [GDI+], GetHalftonePalette method [GDI+],Graphics class, Graphics class [GDI+],GetHalftonePalette method, Graphics.GetHalftonePalette, Graphics::GetHalftonePalette, _gdiplus_CLASS_Graphics_GetHalftonePalette_, gdiplus._gdiplus_CLASS_Graphics_GetHalftonePalette_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.GetHalftonePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetHalftonePalette


## -description


The <b>Graphics::GetHalftonePalette</b> method gets a Windows halftone palette.


## -parameters






## -returns



Type: <strong>Type: <b>static</b>
</strong>

This method returns a handle to a Windows halftone palette.




## -remarks



The purpose of the <b>Graphics::GetHalftonePalette</b> method is to enable GDI+ to produce a better quality halftone when the display uses 8 bits per pixel. To display an image using the halftone palette, use the following procedure: 

<ol>
<li>Call <b>Graphics::GetHalftonePalette</b> to get a GDI+ halftone palette. </li>
<li>Select the halftone palette into a device context. </li>
<li>Realize the palette by calling the 
						<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> function. </li>
<li>Construct a 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object from a handle to the device context. </li>
<li>Call the
<a href="https://msdn.microsoft.com/8eaa8e63-a46c-4453-88a6-838785a55b9f">Graphics::DrawImage</a> method of the 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. </li>
</ol>
Be sure to delete the palette when you have finished using it. If you do not follow the preceding procedure, then on an 8-bits-per-pixel-display device, the default, 16-color process is used, which results in a lesser quality halftone.


#### Examples



The following example draws the same image twice. Before the image is drawn the second time, the code gets a halftone palette, selects the palette into a device context, and realizes the palette.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetHalftonePalette(HDC hdc)
{
   Image image(L"Mosaic.png");
   
   Graphics* graphics1 = new Graphics(hdc);
   graphics1-&gt;DrawImage(&amp;image, 10, 10);
   delete graphics1;
   
   HPALETTE hPalette = Graphics::GetHalftonePalette();
   SelectPalette(hdc, hPalette, FALSE);
   RealizePalette(hdc);
   Graphics* graphics2 = new Graphics(hdc);
   graphics2-&gt;DrawImage(&amp;image, 300, 10);
   delete graphics2;
   DeleteObject(hPalette);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ffe250ce-0ebc-4470-846f-f45a1de5165e">GetPalette</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>



<a href="https://msdn.microsoft.com/62f1c8c0-788b-41e6-91af-15019b65bc3d"> SetPalette</a>
 

 

