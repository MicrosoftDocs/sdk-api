---
UID: NF:dwrite_2.IDWriteFactory2.GetSystemFontFallback
title: IDWriteFactory2::GetSystemFontFallback (dwrite_2.h)
description: Creates a font fallback object from the system font fallback list.
helpviewer_keywords: ["GetSystemFontFallback","GetSystemFontFallback method [Direct Write]","GetSystemFontFallback method [Direct Write]","IDWriteFactory2 interface","IDWriteFactory2 interface [Direct Write]","GetSystemFontFallback method","IDWriteFactory2.GetSystemFontFallback","IDWriteFactory2::GetSystemFontFallback","directwrite.idwritefactory2_getsystemfontfallback","dwrite_2/IDWriteFactory2::GetSystemFontFallback"]
old-location: directwrite\idwritefactory2_getsystemfontfallback.htm
tech.root: DirectWrite
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
ms.date: 12/05/2018
ms.keywords: GetSystemFontFallback, GetSystemFontFallback method [Direct Write], GetSystemFontFallback method [Direct Write],IDWriteFactory2 interface, IDWriteFactory2 interface [Direct Write],GetSystemFontFallback method, IDWriteFactory2.GetSystemFontFallback, IDWriteFactory2::GetSystemFontFallback, directwrite.idwritefactory2_getsystemfontfallback, dwrite_2/IDWriteFactory2::GetSystemFontFallback
req.header: dwrite_2.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFactory2::GetSystemFontFallback
 - dwrite_2/IDWriteFactory2::GetSystemFontFallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_2.h
api_name:
 - IDWriteFactory2.GetSystemFontFallback
---

# IDWriteFactory2::GetSystemFontFallback


## -description

Creates a font fallback object from the system font fallback list.

## -parameters

### -param fontFallback [out]

Type: <b><a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback">IDWriteFontFallback</a>**</b>

Contains an address of a pointer to the newly created font fallback object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefactory2">IDWriteFactory2</a>

