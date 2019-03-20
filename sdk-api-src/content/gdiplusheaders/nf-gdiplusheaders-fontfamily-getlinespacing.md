---
UID: NF:gdiplusheaders.FontFamily.GetLineSpacing
title: FontFamily::GetLineSpacing (gdiplusheaders.h)
author: windows-sdk-content
description: The FontFamily::GetLineSpacing method gets the line spacing, in design units, of this font family for the specified style or style combination. The line spacing is the vertical distance between the base lines of two consecutive lines of text.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetLineSpacing_style_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getlinespacing.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FontFamily class [GDI+],GetLineSpacing method, FontFamily.GetLineSpacing, FontFamily::GetLineSpacing, GetLineSpacing, GetLineSpacing method [GDI+], GetLineSpacing method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetLineSpacing_style_, gdiplus._gdiplus_CLASS_FontFamily_GetLineSpacing_style_
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
 - FontFamily.GetLineSpacing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# FontFamily::GetLineSpacing


## -description


The <b>FontFamily::GetLineSpacing</b> method gets the line spacing, in design units, of this font family for the specified style or style combination. The line spacing is the vertical distance between the base lines of two consecutive lines of text. 


## -parameters




### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534124(v=VS.85).aspx">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> specifies a combination of the three styles. 


## -returns



Type: <strong>Type: <b>UINT16</b>
</strong>

This method returns the line spacing of this font family.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536174(v=VS.85).aspx">FontFamily::GetCellAscent</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536175(v=VS.85).aspx">FontFamily::GetCellDescent</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536176(v=VS.85).aspx">FontFamily::GetEmHeight</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534124(v=VS.85).aspx">FontStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533824(v=VS.85).aspx">Obtaining Font Metrics</a>
 

 

