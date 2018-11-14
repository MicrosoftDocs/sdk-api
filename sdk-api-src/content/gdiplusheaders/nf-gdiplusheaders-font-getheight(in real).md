---
UID: NF:gdiplusheaders.Font.GetHeight(IN REAL)
title: Font::GetHeight(IN REAL)
author: windows-sdk-content
description: The Font::GetHeight method gets the line spacing, in pixels, of this font.
old-location: gdiplus\_gdiplus_CLASS_Font_GetHeight_dpi_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\fontgetheightmethods\getheight_84dpi.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Font class [GDI+],GetHeight method, Font.GetHeight, Font.GetHeight(IN REAL), Font.GetHeight(REAL), Font::GetHeight, Font::GetHeight(IN REAL), GetHeight, GetHeight method [GDI+], GetHeight method [GDI+],Font class, _gdiplus_CLASS_Font_GetHeight_dpi_, gdiplus._gdiplus_CLASS_Font_GetHeight_dpi_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - Font.GetHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Font.GetHeight
: 
req.product: GDI+ 1.0
---

# Font::GetHeight(IN REAL)


## -description


The <b>Font::GetHeight</b> method gets the line spacing, in pixels, of this font. The line spacing is the vertical distance between the base lines of two consecutive lines of text. Thus, the line spacing includes the blank space between lines along with the height of the character itself.


## -parameters




### -param dpi [in]

Type: <b>REAL</b>

Real number that specifies the vertical resolution, in dots per inch, of the device that displays the font. 


## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns the line spacing of the font in pixels.




## -remarks



If the font unit is set to anything other than <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">UnitPixel</a>, the height, in pixels, is calculated using the specified vertical resolution. For example, suppose the font unit is inches and the font size is 0.3. Also suppose that for the corresponding font family, the em height is 2048 and the line spacing is 2355. If the specified vertical resolution is 96 dots per inch, the height is calculated as follows:

2355*(0.3/2048)*96 = 33.1171875




## -see-also




<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/5aa28e74-48e1-47c2-bac0-f2abcdf7b67b">Font::GetSize</a>



<a href="https://msdn.microsoft.com/f3453c5d-7ecb-411f-88a6-fae01cca7dd9">Font::GetStyle</a>



<a href="https://msdn.microsoft.com/3cf901f0-9be9-4dcd-b847-6c3d530556cd">Font::GetUnit</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 

