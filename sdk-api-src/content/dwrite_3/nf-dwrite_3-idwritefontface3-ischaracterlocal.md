---
UID: NF:dwrite_3.IDWriteFontFace3.IsCharacterLocal
title: IDWriteFontFace3::IsCharacterLocal (dwrite_3.h)
description: Determines whether the character is locally downloaded from the font.
helpviewer_keywords: ["IDWriteFontFace3 interface [Direct Write]","IsCharacterLocal method","IDWriteFontFace3.IsCharacterLocal","IDWriteFontFace3::IsCharacterLocal","IsCharacterLocal","IsCharacterLocal method [Direct Write]","IsCharacterLocal method [Direct Write]","IDWriteFontFace3 interface","directwrite.idwritefontface3_ischaracterlocal","dwrite_3/IDWriteFontFace3::IsCharacterLocal"]
old-location: directwrite\idwritefontface3_ischaracterlocal.htm
tech.root: DirectWrite
ms.assetid: 7a47f73b-9ce7-f7db-688b-291cebad54bb
ms.date: 09/10/2025
ms.keywords: IDWriteFontFace3 interface [Direct Write],IsCharacterLocal method, IDWriteFontFace3.IsCharacterLocal, IDWriteFontFace3::IsCharacterLocal, IsCharacterLocal, IsCharacterLocal method [Direct Write], IsCharacterLocal method [Direct Write],IDWriteFontFace3 interface, directwrite.idwritefontface3_ischaracterlocal, dwrite_3/IDWriteFontFace3::IsCharacterLocal
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
 - IDWriteFontFace3::IsCharacterLocal
 - dwrite_3/IDWriteFontFace3::IsCharacterLocal
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
 - IDWriteFontFace3.IsCharacterLocal
---

# IDWriteFontFace3::IsCharacterLocal


## -description

Determines whether the character is locally downloaded from the font.

## -parameters

### -param unicodeValue [in]

Type: <b>UINT32</b>

A Unicode (UCS-4) character value.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the font has the specified character locally available,    
  <b>FALSE</b> if not or if the font does not support that character.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

