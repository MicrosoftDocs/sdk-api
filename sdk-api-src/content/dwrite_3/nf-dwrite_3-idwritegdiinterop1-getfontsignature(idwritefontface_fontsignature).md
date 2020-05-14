---
UID: NF:dwrite_3.IDWriteGdiInterop1.GetFontSignature(IDWriteFontFace,FONTSIGNATURE)
title: IDWriteGdiInterop1::GetFontSignature(IDWriteFontFace,FONTSIGNATURE) (dwrite_3.h)
description: Reads the font signature from the given font.helpviewer_keywords: ["GetFontSignature","GetFontSignature method [Direct Write]","GetFontSignature method [Direct Write]","IDWriteGdiInterop1 interface","IDWriteGdiInterop1 interface [Direct Write]","GetFontSignature method","IDWriteGdiInterop1.GetFontSignature","IDWriteGdiInterop1.GetFontSignature(IDWriteFontFace","FONTSIGNATURE)","IDWriteGdiInterop1::GetFontSignature","IDWriteGdiInterop1::GetFontSignature(IDWriteFontFace","FONTSIGNATURE)","directwrite.idwritegdiinterop1_getfontsignature","dwrite_3/IDWriteGdiInterop1::GetFontSignature"]
old-location: directwrite\idwritegdiinterop1_getfontsignature.htm
tech.root: DirectWrite
ms.assetid: 205EC8E6-233B-4ADB-B6B5-E052CF75277A
ms.date: 12/05/2018
ms.keywords: GetFontSignature, GetFontSignature method [Direct Write], GetFontSignature method [Direct Write],IDWriteGdiInterop1 interface, IDWriteGdiInterop1 interface [Direct Write],GetFontSignature method, IDWriteGdiInterop1.GetFontSignature, IDWriteGdiInterop1.GetFontSignature(IDWriteFontFace,FONTSIGNATURE), IDWriteGdiInterop1::GetFontSignature, IDWriteGdiInterop1::GetFontSignature(IDWriteFontFace,FONTSIGNATURE), directwrite.idwritegdiinterop1_getfontsignature, dwrite_3/IDWriteGdiInterop1::GetFontSignature
f1_keywords:
- dwrite_3/IDWriteGdiInterop1.GetFontSignature
dev_langs:
- c++
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
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteGdiInterop1.GetFontSignature
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteGdiInterop1::GetFontSignature(IDWriteFontFace,FONTSIGNATURE)


## -description


Reads the font signature from the given font.


## -parameters




#### - fontFace [in]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>*</b>

Font to read font signature from.


### -param fontSignature [out]

Type: <b>FONTSIGNATURE*</b>

Font signature from the OS/2 table, ulUnicodeRange and ulCodePageRange.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1">IDWriteGdiInterop1</a>
 

 

