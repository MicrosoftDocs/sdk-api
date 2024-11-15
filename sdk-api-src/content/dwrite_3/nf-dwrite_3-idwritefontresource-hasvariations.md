---
UID: NF:dwrite_3.IDWriteFontResource.HasVariations
title: IDWriteFontResource::HasVariations
description: Determines whether this font face's resource supports any variable axes. (IDWriteFontResource::HasVariations)
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","HasVariations method","IDWriteFontResource.HasVariations","IDWriteFontResource::HasVariations","HasVariations","HasVariations method [Direct Write]","HasVariations method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_hasvariations","dwrite_3/IDWriteFontResource::HasVariations"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],HasVariations method, IDWriteFontResource.HasVariations, IDWriteFontResource::HasVariations, HasVariations, HasVariations method [Direct Write], HasVariations method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_hasvariations, dwrite_3/IDWriteFontResource::HasVariations
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
 - IDWriteFontResource::HasVariations
 - dwrite_3/IDWriteFontResource::HasVariations
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
 - IDWriteFontResource::HasVariations
---

## -description

Determines whether this font face's resource supports any variable axes. When `true`, at least one [DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md) in the font resource has a non-empty range (*maxValue* > *minValue*).



## -returns

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if the font face's resource supports any variable axes. Otherwise, `false`.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md)
