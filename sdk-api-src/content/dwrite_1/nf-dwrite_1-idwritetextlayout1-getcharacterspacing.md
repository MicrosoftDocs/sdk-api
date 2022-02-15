---
UID: NF:dwrite_1.IDWriteTextLayout1.GetCharacterSpacing
title: IDWriteTextLayout1::GetCharacterSpacing (dwrite_1.h)
description: Gets the spacing between characters.
helpviewer_keywords: ["GetCharacterSpacing","GetCharacterSpacing method [Direct Write]","GetCharacterSpacing method [Direct Write]","IDWriteTextLayout1 interface","IDWriteTextLayout1 interface [Direct Write]","GetCharacterSpacing method","IDWriteTextLayout1.GetCharacterSpacing","IDWriteTextLayout1::GetCharacterSpacing","directwrite.idwritetextlayout1_getcharacterspacing","dwrite_1/IDWriteTextLayout1::GetCharacterSpacing"]
old-location: directwrite\idwritetextlayout1_getcharacterspacing.htm
tech.root: DirectWrite
ms.assetid: A546DCB4-8068-4300-94FB-A5B314536869
ms.date: 12/05/2018
ms.keywords: GetCharacterSpacing, GetCharacterSpacing method [Direct Write], GetCharacterSpacing method [Direct Write],IDWriteTextLayout1 interface, IDWriteTextLayout1 interface [Direct Write],GetCharacterSpacing method, IDWriteTextLayout1.GetCharacterSpacing, IDWriteTextLayout1::GetCharacterSpacing, directwrite.idwritetextlayout1_getcharacterspacing, dwrite_1/IDWriteTextLayout1::GetCharacterSpacing
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextLayout1::GetCharacterSpacing
 - dwrite_1/IDWriteTextLayout1::GetCharacterSpacing
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
 - IDWriteTextLayout1.GetCharacterSpacing
---

# IDWriteTextLayout1::GetCharacterSpacing


## -description

Gets the spacing between characters.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The current text position.

### -param leadingSpacing [out]

Type: <b>FLOAT*</b>

The spacing before each character, in reading order.

### -param trailingSpacing [out]

Type: <b>FLOAT*</b>

The spacing after each character, in reading order.

### -param minimumAdvanceWidth [out]

Type: <b>FLOAT*</b>

The minimum advance of each character, to prevent characters from becoming too thin or zero-width. This must be zero or greater.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The position range of the current format.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1">IDWriteTextLayout1</a>

