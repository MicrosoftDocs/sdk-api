---
UID: NF:dwrite.IDWriteFont.HasCharacter
title: IDWriteFont::HasCharacter (dwrite.h)
description: Determines whether the font supports a specified character.
helpviewer_keywords: ["HasCharacter","HasCharacter method [Direct Write]","HasCharacter method [Direct Write]","IDWriteFont interface","IDWriteFont interface [Direct Write]","HasCharacter method","IDWriteFont.HasCharacter","IDWriteFont::HasCharacter","directwrite.IDWriteFont_HasCharacter","dwrite/IDWriteFont::HasCharacter"]
old-location: directwrite\IDWriteFont_HasCharacter.htm
tech.root: DirectWrite
ms.assetid: 5392119a-dfc3-4947-9a0f-fa66ee6359d6
ms.date: 12/05/2018
ms.keywords: HasCharacter, HasCharacter method [Direct Write], HasCharacter method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],HasCharacter method, IDWriteFont.HasCharacter, IDWriteFont::HasCharacter, directwrite.IDWriteFont_HasCharacter, dwrite/IDWriteFont::HasCharacter
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFont::HasCharacter
 - dwrite/IDWriteFont::HasCharacter
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
 - IDWriteFont.HasCharacter
---

# IDWriteFont::HasCharacter


## -description

 Determines whether the font supports a specified character.

## -parameters

### -param unicodeValue

Type: <b>UINT32</b>

A Unicode (UCS-4) character value for the method to inspect.

### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, <b>TRUE</b> if the font supports the specified character; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getunicoderanges">IDWriteFontFace1::GetUnicodeRanges</a>

