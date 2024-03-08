---
UID: NF:dwrite_2.IDWriteTextFormat1.SetFontFallback
title: IDWriteTextFormat1::SetFontFallback (dwrite_2.h)
description: Applies the custom font fallback onto the layout. If none is set, it uses the default system fallback list.
helpviewer_keywords: ["IDWriteTextFormat1 interface [Direct Write]","SetFontFallback method","IDWriteTextFormat1.SetFontFallback","IDWriteTextFormat1::SetFontFallback","SetFontFallback","SetFontFallback method [Direct Write]","SetFontFallback method [Direct Write]","IDWriteTextFormat1 interface","directwrite.idwritetextformat1_setfontfallback","dwrite_2/IDWriteTextFormat1::SetFontFallback"]
old-location: directwrite\idwritetextformat1_setfontfallback.htm
tech.root: DirectWrite
ms.assetid: 56B577C0-2B18-409E-ADEC-0B93355586A0
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat1 interface [Direct Write],SetFontFallback method, IDWriteTextFormat1.SetFontFallback, IDWriteTextFormat1::SetFontFallback, SetFontFallback, SetFontFallback method [Direct Write], SetFontFallback method [Direct Write],IDWriteTextFormat1 interface, directwrite.idwritetextformat1_setfontfallback, dwrite_2/IDWriteTextFormat1::SetFontFallback
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextFormat1::SetFontFallback
 - dwrite_2/IDWriteTextFormat1::SetFontFallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat1.SetFontFallback
---

# IDWriteTextFormat1::SetFontFallback


## -description

Applies the custom font fallback onto the layout. If none is set, it uses the default system fallback list.

## -parameters

### -param fontFallback

Type: <b><a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback">IDWriteFontFallback</a>*</b>

The font fallback to apply to the layout.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextformat1">IDWriteTextFormat1</a>

