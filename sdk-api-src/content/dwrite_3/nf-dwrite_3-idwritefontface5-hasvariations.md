---
UID: NF:dwrite_3.IDWriteFontFace5.HasVariations
title: IDWriteFontFace5::HasVariations
description: Determines whether this font face's resource supports any variable axes. (IDWriteFontFace5::HasVariations)
helpviewer_keywords: ["IDWriteFontFace5 interface [Direct Write]","HasVariations method","IDWriteFontFace5.HasVariations","IDWriteFontFace5::HasVariations","HasVariations","HasVariations method [Direct Write]","HasVariations method [Direct Write]","IDWriteFontFace5 interface","directwrite.idwritefontface5_hasvariations","dwrite_3/IDWriteFontFace5::HasVariations"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5 interface [Direct Write],HasVariations method, IDWriteFontFace5.HasVariations, IDWriteFontFace5::HasVariations, HasVariations, HasVariations method [Direct Write], HasVariations method [Direct Write],IDWriteFontFace5 interface, directwrite.idwritefontface5_hasvariations, dwrite_3/IDWriteFontFace5::HasVariations
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFontFace5::HasVariations
 - dwrite_3/IDWriteFontFace5::HasVariations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace5::HasVariations
---

## -description

Determines whether this font face's resource supports any variable axes. When `true`, at least one [DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md) in the font resource has a non-empty range (*maxValue* > *minValue*).



## -returns

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if the font face's resource supports any variable axes. Otherwise, `false`.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md)
