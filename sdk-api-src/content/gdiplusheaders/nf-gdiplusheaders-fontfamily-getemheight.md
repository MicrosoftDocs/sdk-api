---
UID: NF:gdiplusheaders.FontFamily.GetEmHeight
title: FontFamily::GetEmHeight
author: windows-sdk-content
description: The FontFamily::GetEmHeight method gets the size (commonly called em size or em height), in design units, of this font family.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetEmHeight_style_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getemheight.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FontFamily class [GDI+],GetEmHeight method, FontFamily.GetEmHeight, FontFamily::GetEmHeight, GetEmHeight, GetEmHeight method [GDI+], GetEmHeight method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetEmHeight_style_, gdiplus._gdiplus_CLASS_FontFamily_GetEmHeight_style_
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
 - FontFamily.GetEmHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# FontFamily::GetEmHeight


## -description


The <b>FontFamily::GetEmHeight</b> method gets the size (commonly called em size or em height), in design units, of this font family.


## -parameters




### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534124(v=VS.85).aspx">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> specifies a combination of the three styles. 


## -returns



Type: <strong>Type: <b>UINT16</b>
</strong>

This method returns the size, in design units, of this font family.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536175(v=VS.85).aspx">FontFamily::GetCellDescent</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536176(v=VS.85).aspx">FontFamily::GetEmHeight</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536179(v=VS.85).aspx">FontFamily::GetLineSpacing</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534124(v=VS.85).aspx">FontStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533824(v=VS.85).aspx">Obtaining Font Metrics</a>
 

 

