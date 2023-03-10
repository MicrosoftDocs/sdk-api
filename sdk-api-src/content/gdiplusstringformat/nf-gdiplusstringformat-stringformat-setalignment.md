---
UID: NF:gdiplusstringformat.StringFormat.SetAlignment
title: StringFormat::SetAlignment (gdiplusstringformat.h)
description: The StringFormat::SetAlignment method sets the character alignment of this StringFormat object in relation to the origin of the layout rectangle. A layout rectangle is used to position the displayed string.
helpviewer_keywords: ["SetAlignment","SetAlignment method [GDI+]","SetAlignment method [GDI+]","StringFormat class","StringFormat class [GDI+]","SetAlignment method","StringFormat.SetAlignment","StringFormat::SetAlignment","_gdiplus_CLASS_StringFormat_SetAlignment_align_","gdiplus._gdiplus_CLASS_StringFormat_SetAlignment_align_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetAlignment_align_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setalignment_24align.htm
ms.date: 12/05/2018
ms.keywords: SetAlignment, SetAlignment method [GDI+], SetAlignment method [GDI+],StringFormat class, StringFormat class [GDI+],SetAlignment method, StringFormat.SetAlignment, StringFormat::SetAlignment, _gdiplus_CLASS_StringFormat_SetAlignment_align_, gdiplus._gdiplus_CLASS_StringFormat_SetAlignment_align_
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
 - StringFormat::SetAlignment
 - gdiplusstringformat/StringFormat::SetAlignment
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
 - StringFormat.SetAlignment
---

# StringFormat::SetAlignment


## -description

The <b>StringFormat::SetAlignment</b> method sets the character alignment of this 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object in relation to the origin of the layout rectangle. A layout rectangle is used to position the displayed string.

## -parameters

### -param align [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a> enumeration that specifies how a string is aligned in reference to the bounding rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>