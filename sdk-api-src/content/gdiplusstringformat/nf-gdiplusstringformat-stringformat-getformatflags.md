---
UID: NF:gdiplusstringformat.StringFormat.GetFormatFlags
title: StringFormat::GetFormatFlags (gdiplusstringformat.h)
description: The StringFormat::GetFormatFlags method gets the string format flags for this StringFormat object.
helpviewer_keywords: ["GetFormatFlags","GetFormatFlags method [GDI+]","GetFormatFlags method [GDI+]","StringFormat class","StringFormat class [GDI+]","GetFormatFlags method","StringFormat.GetFormatFlags","StringFormat::GetFormatFlags","_gdiplus_CLASS_StringFormat_GetFormatFlags_","gdiplus._gdiplus_CLASS_StringFormat_GetFormatFlags_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GetFormatFlags_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\getformatflags.htm
ms.date: 12/05/2018
ms.keywords: GetFormatFlags, GetFormatFlags method [GDI+], GetFormatFlags method [GDI+],StringFormat class, StringFormat class [GDI+],GetFormatFlags method, StringFormat.GetFormatFlags, StringFormat::GetFormatFlags, _gdiplus_CLASS_StringFormat_GetFormatFlags_, gdiplus._gdiplus_CLASS_StringFormat_GetFormatFlags_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - StringFormat::GetFormatFlags
 - gdiplusstringformat/StringFormat::GetFormatFlags
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
 - StringFormat.GetFormatFlags
---

# StringFormat::GetFormatFlags


## -description

The <b>StringFormat::GetFormatFlags</b> method gets the string format flags for this 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.



## -returns

Type: <b>INT</b>

This method returns a value that indicates which string format flags are set for this 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object. This value can be any combination (the result of a bitwise 
						<b>OR</b> applied to two or more elements) of elements of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a>
