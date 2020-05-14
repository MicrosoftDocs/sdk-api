---
UID: NF:dwrite_3.IDWriteFontFace5.GetFontAxisValueCount
title: IDWriteFontFace5::GetFontAxisValueCount
description: Retrieves the number of axes defined by the font. This includes both static and variable axes.helpviewer_keywords: ["IDWriteFontFace5 interface [Direct Write]","GetFontAxisValueCount method","IDWriteFontFace5.GetFontAxisValueCount","IDWriteFontFace5::GetFontAxisValueCount","GetFontAxisValueCount","GetFontAxisValueCount method [Direct Write]","GetFontAxisValueCount method [Direct Write]","IDWriteFontFace5 interface","directwrite.idwritefontface5_getfontaxisvaluecount","dwrite_3/IDWriteFontFace5::GetFontAxisValueCount"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5 interface [Direct Write],GetFontAxisValueCount method, IDWriteFontFace5.GetFontAxisValueCount, IDWriteFontFace5::GetFontAxisValueCount, GetFontAxisValueCount, GetFontAxisValueCount method [Direct Write], GetFontAxisValueCount method [Direct Write],IDWriteFontFace5 interface, directwrite.idwritefontface5_getfontaxisvaluecount, dwrite_3/IDWriteFontFace5::GetFontAxisValueCount
f1_keywords:
- dwrite_3/IDWriteFontFace5.GetFontAxisValueCount
dev_langs:
- c++
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
- IDWriteFontFace5::GetFontAxisValueCount
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the number of axes defined by the font face. This includes both static and variable axes (see [DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)).

## -returns

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of axes defined by the font face.

## -remarks

## -see-also

[DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
