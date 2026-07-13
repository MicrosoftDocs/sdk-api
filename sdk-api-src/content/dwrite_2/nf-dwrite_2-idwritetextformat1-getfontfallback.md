---
UID: NF:dwrite_2.IDWriteTextFormat1.GetFontFallback
title: IDWriteTextFormat1::GetFontFallback (dwrite_2.h)
description: Gets the current fallback. If none was ever set since creating the layout, it will be nullptr.
helpviewer_keywords: ["GetFontFallback","GetFontFallback method [Direct Write]","GetFontFallback method [Direct Write]","IDWriteTextFormat1 interface","IDWriteTextFormat1 interface [Direct Write]","GetFontFallback method","IDWriteTextFormat1.GetFontFallback","IDWriteTextFormat1::GetFontFallback","directwrite.idwritetextformat1_getfontfallback","dwrite_2/IDWriteTextFormat1::GetFontFallback"]
old-location: directwrite\idwritetextformat1_getfontfallback.htm
tech.root: DirectWrite
ms.assetid: D34A49A0-CE37-43B9-B7CC-6A70D76BA369
ms.date: 12/05/2018
ms.keywords: GetFontFallback, GetFontFallback method [Direct Write], GetFontFallback method [Direct Write],IDWriteTextFormat1 interface, IDWriteTextFormat1 interface [Direct Write],GetFontFallback method, IDWriteTextFormat1.GetFontFallback, IDWriteTextFormat1::GetFontFallback, directwrite.idwritetextformat1_getfontfallback, dwrite_2/IDWriteTextFormat1::GetFontFallback
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
 - IDWriteTextFormat1::GetFontFallback
 - dwrite_2/IDWriteTextFormat1::GetFontFallback
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
 - IDWriteTextFormat1.GetFontFallback
---

# IDWriteTextFormat1::GetFontFallback


## -description

Gets the current fallback. If none was ever set since creating the layout, it will be nullptr.

## -parameters

### -param fontFallback [out]

Type: <b><a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback">IDWriteFontFallback</a>**</b>

Contains an address of a pointer to the current font fallback object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextformat1">IDWriteTextFormat1</a>

