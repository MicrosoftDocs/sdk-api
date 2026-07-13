---
UID: NF:dwrite.IDWriteTextLayout.GetFontFamilyNameLength
title: IDWriteTextLayout::GetFontFamilyNameLength (dwrite.h)
description: Get the length of the font family name at the current position.
helpviewer_keywords: ["GetFontFamilyNameLength","GetFontFamilyNameLength method [Direct Write]","GetFontFamilyNameLength method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontFamilyNameLength method","IDWriteTextLayout.GetFontFamilyNameLength","IDWriteTextLayout::GetFontFamilyNameLength","directwrite.IDWriteTextLayout_GetFontFamilyNameLength","dwrite/IDWriteTextLayout::GetFontFamilyNameLength"]
old-location: directwrite\IDWriteTextLayout_GetFontFamilyNameLength.htm
tech.root: DirectWrite
ms.assetid: e3b3d111-04a7-409b-98dd-b0fc3947f24b
ms.date: 12/05/2018
ms.keywords: GetFontFamilyNameLength, GetFontFamilyNameLength method [Direct Write], GetFontFamilyNameLength method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontFamilyNameLength method, IDWriteTextLayout.GetFontFamilyNameLength, IDWriteTextLayout::GetFontFamilyNameLength, directwrite.IDWriteTextLayout_GetFontFamilyNameLength, dwrite/IDWriteTextLayout::GetFontFamilyNameLength
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
 - IDWriteTextLayout::GetFontFamilyNameLength
 - dwrite/IDWriteTextLayout::GetFontFamilyNameLength
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
 - IDWriteTextLayout.GetFontFamilyNameLength
---

# IDWriteTextLayout::GetFontFamilyNameLength


## -description

 Get the length of the font family name at the current position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The current text position.

### -param nameLength [out]

Type: <b>UINT32*</b>

When this method returns, contains the size of the character array containing the font family name, in character count, not including the terminated <b>NULL</b> character.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font family.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

