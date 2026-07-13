---
UID: NF:dwrite_2.IDWriteTextLayout2.SetFontFallback
title: IDWriteTextLayout2::SetFontFallback (dwrite_2.h)
description: Apply a custom font fallback onto layout.
helpviewer_keywords: ["IDWriteTextLayout2 interface [Direct Write]","SetFontFallback method","IDWriteTextLayout2.SetFontFallback","IDWriteTextLayout2::SetFontFallback","SetFontFallback","SetFontFallback method [Direct Write]","SetFontFallback method [Direct Write]","IDWriteTextLayout2 interface","directwrite.idwritetextlayout2_setfontfallback","dwrite_2/IDWriteTextLayout2::SetFontFallback"]
old-location: directwrite\idwritetextlayout2_setfontfallback.htm
tech.root: DirectWrite
ms.assetid: 63B86AE4-92D4-4748-A6E2-987B740080EB
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout2 interface [Direct Write],SetFontFallback method, IDWriteTextLayout2.SetFontFallback, IDWriteTextLayout2::SetFontFallback, SetFontFallback, SetFontFallback method [Direct Write], SetFontFallback method [Direct Write],IDWriteTextLayout2 interface, directwrite.idwritetextlayout2_setfontfallback, dwrite_2/IDWriteTextLayout2::SetFontFallback
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDWriteTextLayout2::SetFontFallback
 - dwrite_2/IDWriteTextLayout2::SetFontFallback
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
 - IDWriteTextLayout2.SetFontFallback
---

# IDWriteTextLayout2::SetFontFallback


## -description

Apply a custom font fallback onto layout. If none is specified, the layout uses the system fallback list.

## -parameters

### -param fontFallback

Custom font fallback created from <a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback">IDWriteFontFallbackBuilder::CreateFontFallback</a> or <a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-getsystemfontfallback">IDWriteFactory2::GetSystemFontFallback</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextlayout2">IDWriteTextLayout2</a>

