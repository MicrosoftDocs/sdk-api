---
UID: NF:gdiplusstringformat.StringFormat.SetLineAlignment
title: StringFormat::SetLineAlignment (gdiplusstringformat.h)
description: The StringFormat::SetLineAlignment method sets the line alignment of this StringFormat object in relation to the origin of the layout rectangle.
helpviewer_keywords: ["SetLineAlignment","SetLineAlignment method [GDI+]","SetLineAlignment method [GDI+]","StringFormat class","StringFormat class [GDI+]","SetLineAlignment method","StringFormat.SetLineAlignment","StringFormat::SetLineAlignment","_gdiplus_CLASS_StringFormat_SetLineAlignment_align_","gdiplus._gdiplus_CLASS_StringFormat_SetLineAlignment_align_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetLineAlignment_align_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setlinealignment.htm
ms.date: 12/05/2018
ms.keywords: SetLineAlignment, SetLineAlignment method [GDI+], SetLineAlignment method [GDI+],StringFormat class, StringFormat class [GDI+],SetLineAlignment method, StringFormat.SetLineAlignment, StringFormat::SetLineAlignment, _gdiplus_CLASS_StringFormat_SetLineAlignment_align_, gdiplus._gdiplus_CLASS_StringFormat_SetLineAlignment_align_
f1_keywords:
- gdiplusstringformat/StringFormat.SetLineAlignment
dev_langs:
- c++
req.header: gdiplusstringformat.h
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
- StringFormat.SetLineAlignment
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# StringFormat::SetLineAlignment


## -description


The <b>StringFormat::SetLineAlignment</b> method sets the line alignment of this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object in relation to the origin of the layout rectangle. The line alignment setting specifies how to align the string vertically in the layout rectangle. The layout rectangle is used to position the displayed string.


## -parameters




### -param align [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a> enumeration that specifies how to align a string in reference to the layout rectangle. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a>
 

 

