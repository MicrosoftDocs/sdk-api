---
UID: NF:gdiplusheaders.FontFamily.GetCellAscent
title: FontFamily::GetCellAscent
author: windows-sdk-content
description: The FontFamily::GetCellAscent method gets the cell ascent, in design units, of this font family for the specified style or style combination.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetCellAscent_style_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getcellascent.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FontFamily class [GDI+],GetCellAscent method, FontFamily.GetCellAscent, FontFamily::GetCellAscent, GetCellAscent, GetCellAscent method [GDI+], GetCellAscent method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetCellAscent_style_, gdiplus._gdiplus_CLASS_FontFamily_GetCellAscent_style_
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
 - FontFamily.GetCellAscent
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# FontFamily::GetCellAscent


## -description


The <b>FontFamily::GetCellAscent</b> method gets the cell ascent, in design units, of this font family for the specified style or style combination.


## -parameters




### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/library/ms534124(v=VS.85).aspx">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> specifies a combination of the three styles. 


## -returns



Type: <strong>Type: <b>UINT16</b>
</strong>

This method returns the cell ascent, in design units, of this font family for the specified style or style combination.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/library/ms536175(v=VS.85).aspx">FontFamily::GetCellDescent</a>



<a href="https://msdn.microsoft.com/library/ms536176(v=VS.85).aspx">FontFamily::GetEmHeight</a>



<a href="https://msdn.microsoft.com/library/ms536179(v=VS.85).aspx">FontFamily::GetLineSpacing</a>



<a href="https://msdn.microsoft.com/library/ms534124(v=VS.85).aspx">FontStyle</a>



<a href="https://msdn.microsoft.com/library/ms533824(v=VS.85).aspx">Obtaining Font Metrics</a>
 

 

