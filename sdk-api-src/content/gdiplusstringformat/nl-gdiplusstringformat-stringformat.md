---
UID: NL:gdiplusstringformat.StringFormat
title: StringFormat (gdiplusstringformat.h)
description: The StringFormat class encapsulates text layout information (such as alignment, orientation, tab stops, and clipping) and display manipulations (such as trimming, font substitution for characters that are not supported by the requested font, and digit substitution for languages that do not use Western European digits). A StringFormat object can be passed to the DrawString Methods method to format a string.
helpviewer_keywords: ["StringFormat","StringFormat class [GDI+]","StringFormat class [GDI+]","described","_gdiplus_CLASS_StringFormat_Class","gdiplus._gdiplus_CLASS_StringFormat_Class","gdiplusstringformat/StringFormat"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformat.htm
ms.date: 12/05/2018
ms.keywords: StringFormat, StringFormat class [GDI+], StringFormat class [GDI+],described, _gdiplus_CLASS_StringFormat_Class, gdiplus._gdiplus_CLASS_StringFormat_Class, gdiplusstringformat/StringFormat
req.header: gdiplusstringformat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StringFormat
 - gdiplusstringformat/StringFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusstringformat.h
api_name:
 - StringFormat
---

# StringFormat class


## -description

The <b>StringFormat</b> class encapsulates text layout information (such as alignment, orientation, tab stops, and clipping) and display manipulations (such as trimming, font substitution for characters that are not supported by the requested font, and digit substitution for languages that do not use Western European digits). A <b>StringFormat</b> object can be passed to the 
			<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)">DrawString Methods</a>  method to format a string.