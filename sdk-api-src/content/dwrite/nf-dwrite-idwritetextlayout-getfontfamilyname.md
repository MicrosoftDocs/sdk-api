---
UID: NF:dwrite.IDWriteTextLayout.GetFontFamilyName
title: IDWriteTextLayout::GetFontFamilyName (dwrite.h)
description: Copies the font family name of the text at the specified position.
helpviewer_keywords: ["GetFontFamilyName","GetFontFamilyName method [Direct Write]","GetFontFamilyName method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontFamilyName method","IDWriteTextLayout.GetFontFamilyName","IDWriteTextLayout::GetFontFamilyName","directwrite.IDWriteTextLayout_GetFontFamilyName","dwrite/IDWriteTextLayout::GetFontFamilyName"]
old-location: directwrite\IDWriteTextLayout_GetFontFamilyName.htm
tech.root: DirectWrite
ms.assetid: c5283d1f-8a40-4272-b71c-590b6bc6a340
ms.date: 12/05/2018
ms.keywords: GetFontFamilyName, GetFontFamilyName method [Direct Write], GetFontFamilyName method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontFamilyName method, IDWriteTextLayout.GetFontFamilyName, IDWriteTextLayout::GetFontFamilyName, directwrite.IDWriteTextLayout_GetFontFamilyName, dwrite/IDWriteTextLayout::GetFontFamilyName
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
 - IDWriteTextLayout::GetFontFamilyName
 - dwrite/IDWriteTextLayout::GetFontFamilyName
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
 - IDWriteTextLayout.GetFontFamilyName
---

# IDWriteTextLayout::GetFontFamilyName


## -description

 Copies the font family name of the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to examine.

### -param fontFamilyName [out]

Type: <b>WCHAR*</b>

When this method returns, contains an array of characters that receives the current font family name. You must allocate storage for this parameter.

### -param nameSize

Type: <b>UINT32</b>

The size of the character array in character count including the terminated <b>NULL</b> character.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font family name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

