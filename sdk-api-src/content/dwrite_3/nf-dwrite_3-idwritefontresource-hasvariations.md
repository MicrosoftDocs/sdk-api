---
UID: NF:dwrite_3.IDWriteFontResource.HasVariations
title: IDWriteFontResource::HasVariations
author: windows-sdk-content
description: Determines whether this font face's resource supports any variable axes.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],HasVariations method, IDWriteFontResource.HasVariations, IDWriteFontResource::HasVariations, HasVariations, HasVariations method [Direct Write], HasVariations method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_hasvariations, dwrite_3/IDWriteFontResource::HasVariations
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontResource.HasVariations"
req.construct-type: function
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Determines whether this font face's resource supports any variable axes. When `true`, at least one [DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) in the font resource has a non-empty range (*maxValue* > *minValue*).

## -returns

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if the font face's resource supports any variable axes. Otherwise, `false`.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)