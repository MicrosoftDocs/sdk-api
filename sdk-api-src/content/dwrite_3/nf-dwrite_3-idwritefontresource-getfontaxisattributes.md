---
UID: NF:dwrite_3.IDWriteFontResource.GetFontAxisAttributes
title: IDWriteFontResource::GetFontAxisAttributes
description: Retrieves attributes describing the given axis, such as whether the font author recommends to hide the axis in user interfaces.
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","GetFontAxisAttributes method","IDWriteFontResource.GetFontAxisAttributes","IDWriteFontResource::GetFontAxisAttributes","GetFontAxisAttributes","GetFontAxisAttributes method [Direct Write]","GetFontAxisAttributes method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_getfontaxisattributes","dwrite_3/IDWriteFontResource::GetFontAxisAttributes"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFontResource interface [Direct Write],GetFontAxisAttributes method, IDWriteFontResource.GetFontAxisAttributes, IDWriteFontResource::GetFontAxisAttributes, GetFontAxisAttributes, GetFontAxisAttributes method [Direct Write], GetFontAxisAttributes method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getfontaxisattributes, dwrite_3/IDWriteFontResource::GetFontAxisAttributes
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
 - IDWriteFontResource::GetFontAxisAttributes
 - dwrite_3/IDWriteFontResource::GetFontAxisAttributes
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
 - IDWriteFontResource::GetFontAxisAttributes
---

## -description

Retrieves attributes describing the given axis, such as whether the font author recommends to hide the axis in user interfaces.

## -parameters

### -param axisIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Font axis, from 0 to [GetFontAxisCount](./nf-dwrite_3-idwritefontresource-getfontaxiscount.md) minus 1.

## -returns

Type: **[DWRITE_FONT_AXIS_ATTRIBUTES](./ne-dwrite_3-dwrite_font_axis_attributes.md)**

The attributes for the given axis, or **DWRITE_FONT_AXIS_ATTRIBUTES_NONE** if *axisIndex* is beyond the font count.

## -remarks

## -see-also
