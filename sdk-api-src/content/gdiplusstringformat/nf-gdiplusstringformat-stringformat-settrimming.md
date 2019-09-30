---
UID: NF:gdiplusstringformat.StringFormat.SetTrimming
title: StringFormat::SetTrimming (gdiplusstringformat.h)
author: windows-sdk-content
description: The StringFormat::SetTrimming method sets the trimming style for this StringFormat object. The trimming style determines how to trim a string so that it fits into the layout rectangle.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetTrimming_trimming_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\settrimming.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetTrimming, SetTrimming method [GDI+], SetTrimming method [GDI+],StringFormat class, StringFormat class [GDI+],SetTrimming method, StringFormat.SetTrimming, StringFormat::SetTrimming, _gdiplus_CLASS_StringFormat_SetTrimming_trimming_, gdiplus._gdiplus_CLASS_StringFormat_SetTrimming_trimming_
ms.topic: method
f1_keywords: 
 - "gdiplusstringformat/StringFormat.SetTrimming"
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
 - StringFormat.SetTrimming
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# StringFormat::SetTrimming


## -description


The <b>StringFormat::SetTrimming</b> method sets the trimming style for this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object. The trimming style determines how to trim a string so that it fits into the layout rectangle.


## -parameters




### -param trimming [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringtrimming">StringTrimming</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringtrimming">StringTrimming</a> enumeration that specifies the style of trimming to be performed on the string. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringtrimming">StringTrimming</a>
 

 

