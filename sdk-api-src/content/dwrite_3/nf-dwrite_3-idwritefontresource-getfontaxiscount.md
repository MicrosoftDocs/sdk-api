---
UID: NF:dwrite_3.IDWriteFontResource.GetFontAxisCount
title: IDWriteFontResource::GetFontAxisCount
description: Retrieves the number of axes supported by the font resource.
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","GetFontAxisCount method","IDWriteFontResource.GetFontAxisCount","IDWriteFontResource::GetFontAxisCount","GetFontAxisCount","GetFontAxisCount method [Direct Write]","GetFontAxisCount method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_getfontaxiscount","dwrite_3/IDWriteFontResource::GetFontAxisCount"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetFontAxisCount method, IDWriteFontResource.GetFontAxisCount, IDWriteFontResource::GetFontAxisCount, GetFontAxisCount, GetFontAxisCount method [Direct Write], GetFontAxisCount method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getfontaxiscount, dwrite_3/IDWriteFontResource::GetFontAxisCount
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
 - IDWriteFontResource::GetFontAxisCount
 - dwrite_3/IDWriteFontResource::GetFontAxisCount
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
 - IDWriteFontResource::GetFontAxisCount
---

## -description

Retrieves the number of axes supported by the font resource. This includes both static and variable axes (see [DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md)).



## -returns

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of axes defined by the font face.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md)
