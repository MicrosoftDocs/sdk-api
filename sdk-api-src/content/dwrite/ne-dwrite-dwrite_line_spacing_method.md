---
UID: NE:dwrite.DWRITE_LINE_SPACING_METHOD
title: DWRITE_LINE_SPACING_METHOD (dwrite.h)
description: The method used for line spacing in a text layout.
helpviewer_keywords: ["DWRITE_LINE_SPACING_METHOD","DWRITE_LINE_SPACING_METHOD enumeration [Direct Write]","DWRITE_LINE_SPACING_METHOD_DEFAULT","DWRITE_LINE_SPACING_METHOD_PROPORTIONAL","DWRITE_LINE_SPACING_METHOD_UNIFORM","directwrite.dwrite_line_spacing_method","dwrite/DWRITE_LINE_SPACING_METHOD","dwrite/DWRITE_LINE_SPACING_METHOD_DEFAULT","dwrite/DWRITE_LINE_SPACING_METHOD_PROPORTIONAL","dwrite/DWRITE_LINE_SPACING_METHOD_UNIFORM"]
old-location: directwrite\dwrite_line_spacing_method.htm
tech.root: DirectWrite
ms.assetid: b75e8fee-ed6c-455d-8733-e6972792572c
ms.date: 12/05/2018
ms.keywords: DWRITE_LINE_SPACING_METHOD, DWRITE_LINE_SPACING_METHOD enumeration [Direct Write], DWRITE_LINE_SPACING_METHOD_DEFAULT, DWRITE_LINE_SPACING_METHOD_PROPORTIONAL, DWRITE_LINE_SPACING_METHOD_UNIFORM, directwrite.dwrite_line_spacing_method, dwrite/DWRITE_LINE_SPACING_METHOD, dwrite/DWRITE_LINE_SPACING_METHOD_DEFAULT, dwrite/DWRITE_LINE_SPACING_METHOD_PROPORTIONAL, dwrite/DWRITE_LINE_SPACING_METHOD_UNIFORM
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_LINE_SPACING_METHOD
 - dwrite/DWRITE_LINE_SPACING_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_LINE_SPACING_METHOD
---

## -description

The method used for line spacing in a text layout.

## -enum-fields

### -field DWRITE_LINE_SPACING_METHOD_DEFAULT

Line spacing depends solely on the content, adjusting to accommodate the size of fonts and inline objects.

### -field DWRITE_LINE_SPACING_METHOD_UNIFORM

Lines are explicitly set to uniform spacing, regardless of the size of fonts and inline objects. This can be useful to avoid the uneven appearance that can occur from font fallback.

### -field DWRITE_LINE_SPACING_METHOD_PROPORTIONAL

Line spacing and baseline distances are proportional to the computed values based on the content, the size of the fonts and inline objects.

> [!NOTE]
> This value is available only on Windows 10 or later, and it can be used with [IDWriteTextLayout3::SetLineSpacing](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextlayout3-setlinespacing), but it can't be used with [IDWriteTextFormat::SetLineSpacing](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setlinespacing).

## -remarks

The line spacing method is set by using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setlinespacing">SetLineSpacing</a> method of the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a> or <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> interfaces.  To get  the current line spacing method of a text format or text layout use the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-getlinespacing">GetLineSpacing</a>.

## -see-also

<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-getlinespacing">GetLineSpacing</a>



<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setlinespacing">SetLineSpacing</a>

