---
UID: NF:dwrite_3.IDWriteFontFace3.HasCharacter
title: IDWriteFontFace3::HasCharacter (dwrite_3.h)
description: Determines whether the font supports the specified character.
helpviewer_keywords: ["HasCharacter","HasCharacter method [Direct Write]","HasCharacter method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","HasCharacter method","IDWriteFontFace3.HasCharacter","IDWriteFontFace3::HasCharacter","directwrite.idwritefontface3_hascharacter","dwrite_3/IDWriteFontFace3::HasCharacter"]
old-location: directwrite\idwritefontface3_hascharacter.htm
tech.root: DirectWrite
ms.assetid: BCBC382E-C599-429A-9E00-EAB12D675503
ms.date: 09/10/2025
ms.keywords: HasCharacter, HasCharacter method [Direct Write], HasCharacter method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],HasCharacter method, IDWriteFontFace3.HasCharacter, IDWriteFontFace3::HasCharacter, directwrite.idwritefontface3_hascharacter, dwrite_3/IDWriteFontFace3::HasCharacter
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFace3::HasCharacter
 - dwrite_3/IDWriteFontFace3::HasCharacter
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
 - IDWriteFontFace3.HasCharacter
---

# IDWriteFontFace3::HasCharacter


## -description

Determines whether the font supports the specified character.

## -parameters

### -param unicodeValue [in]

Type: <b>UINT32</b>

A Unicode (UCS-4) character value.

## -returns

Type: <b>BOOL</b>

Returns whether the font supports the specified character. Returns <b>TRUE</b> if the font has the specified character; otherwise, <b>FALSE</b>.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

