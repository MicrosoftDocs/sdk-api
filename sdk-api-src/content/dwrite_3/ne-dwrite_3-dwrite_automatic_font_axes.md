---
UID: NE:dwrite_3.DWRITE_AUTOMATIC_FONT_AXES
title: DWRITE_AUTOMATIC_FONT_AXES
description: Defines constants that specify certain axes that can be applied automatically in layout during font selection.
helpviewer_keywords: ["DWRITE_AUTOMATIC_FONT_AXES","DWRITE_AUTOMATIC_FONT_AXES enumeration [Direct Write]","directwrite.dwrite_automatic_font_axes","dwrite_3/DWRITE_AUTOMATIC_FONT_AXES"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: DWRITE_AUTOMATIC_FONT_AXES, DWRITE_AUTOMATIC_FONT_AXES enumeration [Direct Write], directwrite.dwrite_automatic_font_axes, dwrite_3/DWRITE_AUTOMATIC_FONT_AXES
req.construct-type: enumeration
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - DWRITE_AUTOMATIC_FONT_AXES
 - dwrite_3/DWRITE_AUTOMATIC_FONT_AXES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_AUTOMATIC_FONT_AXES
---

## -description

Defines constants that specifies axes that can be applied automatically in layout during font selection. Values can be bitwise OR'd together.

## -enum-fields

### -field DWRITE_AUTOMATIC_FONT_AXES_NONE:0x0000

Specifies that no axes are automatically applied.

### -field DWRITE_AUTOMATIC_FONT_AXES_OPTICAL_SIZE:0x0001

Specifies that&mdash;when no value is specified via <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag">DWRITE_FONT_AXIS_TAG_OPTICAL_SIZE</a>&mdash;an appropriate optical value should be automatically chosen based on the font size (via <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize">IDWriteTextLayout::SetFontSize</a>). You can still apply the 'opsz' value over text ranges via <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat3-setfontaxisvalues">IDWriteTextFormat3::SetFontAxisValues</a>, which take priority.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_TAG enumeration](./ne-dwrite_3-dwrite_font_axis_tag.md)

[IDWriteTextFormat3::SetFontAxisValues](./nf-dwrite_3-idwritetextformat3-setfontaxisvalues.md)
