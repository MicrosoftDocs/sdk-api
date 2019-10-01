---
UID: NF:gdiplusheaders.FontFamily.GetCellDescent
title: FontFamily::GetCellDescent (gdiplusheaders.h)
author: windows-sdk-content
description: The FontFamily::GetCellDescent method gets the cell descent, in design units, of this font family for the specified style or style combination.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetCellDescent_style_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getcelldescent.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FontFamily class [GDI+],GetCellDescent method, FontFamily.GetCellDescent, FontFamily::GetCellDescent, GetCellDescent, GetCellDescent method [GDI+], GetCellDescent method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetCellDescent_style_, gdiplus._gdiplus_CLASS_FontFamily_GetCellDescent_style_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/FontFamily.GetCellDescent"
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
 - FontFamily.GetCellDescent
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# FontFamily::GetCellDescent


## -description


The <b>FontFamily::GetCellDescent</b> method gets the cell descent, in design units, of this font family for the specified style or style combination.


## -parameters




### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> specifies a combination of the three styles. 


## -returns



Type: <strong>Type: <b>UINT16</b>
</strong>

This method returns the cell descent, in design units, of this font family for the specified style or style combination.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent">FontFamily::GetCellDescent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight">FontFamily::GetEmHeight</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing">FontFamily::GetLineSpacing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-obtaining-font-metrics-use">Obtaining Font Metrics</a>
 

 

