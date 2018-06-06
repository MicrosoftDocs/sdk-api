---
UID: NF:gdiplusheaders.FontFamily.GetLineSpacing
title: FontFamily::GetLineSpacing
author: windows-sdk-content
description: The FontFamily::GetLineSpacing method gets the line spacing, in design units, of this font family for the specified style or style combination. The line spacing is the vertical distance between the base lines of two consecutive lines of text.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetLineSpacing_style_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getlinespacing.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FontFamily class [GDI+],GetLineSpacing method, FontFamily.GetLineSpacing, FontFamily::GetLineSpacing, GetLineSpacing, GetLineSpacing method [GDI+], GetLineSpacing method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetLineSpacing_style_, gdiplus._gdiplus_CLASS_FontFamily_GetLineSpacing_style_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - FontFamily.GetLineSpacing
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# FontFamily::GetLineSpacing


## -description


The <b>FontFamily::GetLineSpacing</b> method gets the line spacing, in design units, of this font family for the specified style or style combination. The line spacing is the vertical distance between the base lines of two consecutive lines of text. 


## -parameters




### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> specifies a combination of the three styles. 


## -returns



Type: <strong>Type: <b>UINT16</b>
</strong>

This method returns the line spacing of this font family.




## -see-also




<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>



<a href="https://msdn.microsoft.com/80f615c6-2edb-4c23-8759-8765acf6c403">FontFamily::GetCellAscent</a>



<a href="https://msdn.microsoft.com/f1ddea8e-3964-4a58-955d-a879efe1a6b0">FontFamily::GetCellDescent</a>



<a href="https://msdn.microsoft.com/be56c53d-6708-438d-a703-d0c3f57f170b">FontFamily::GetEmHeight</a>



<a href="https://msdn.microsoft.com/de08c779-1f43-4740-b2b9-8d3906dc4432">FontStyle</a>



<a href="https://msdn.microsoft.com/3be485d0-9e0d-43e0-813e-668102ebc010">Obtaining Font Metrics</a>
 

 

