---
UID: NF:dwrite.IDWriteTextFormat.GetFontFamilyName
title: IDWriteTextFormat::GetFontFamilyName (dwrite.h)
description: Gets a copy of the font family name.
helpviewer_keywords: ["GetFontFamilyName","GetFontFamilyName method [Direct Write]","GetFontFamilyName method [Direct Write]","IDWriteTextFormat interface","IDWriteTextFormat interface [Direct Write]","GetFontFamilyName method","IDWriteTextFormat.GetFontFamilyName","IDWriteTextFormat::GetFontFamilyName","directwrite.IDWriteTextFormat_GetFontFamilyName","dwrite/IDWriteTextFormat::GetFontFamilyName"]
old-location: directwrite\IDWriteTextFormat_GetFontFamilyName.htm
tech.root: DirectWrite
ms.assetid: 44d294bf-ec0f-4c75-b10a-2f3e4883b58a
ms.date: 12/05/2018
ms.keywords: GetFontFamilyName, GetFontFamilyName method [Direct Write], GetFontFamilyName method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetFontFamilyName method, IDWriteTextFormat.GetFontFamilyName, IDWriteTextFormat::GetFontFamilyName, directwrite.IDWriteTextFormat_GetFontFamilyName, dwrite/IDWriteTextFormat::GetFontFamilyName
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
 - IDWriteTextFormat::GetFontFamilyName
 - dwrite/IDWriteTextFormat::GetFontFamilyName
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
 - IDWriteTextFormat.GetFontFamilyName
---

# IDWriteTextFormat::GetFontFamilyName


## -description

 Gets a copy of the font family name.

## -parameters

### -param fontFamilyName [out]

Type: <b>WCHAR*</b>

When this method returns, contains a pointer to a character array, which is null-terminated, that receives the current font family name. The buffer allocated for this array should be at least the size, in elements, of <i>nameSize</i>.

### -param nameSize

Type: <b>UINT32</b>

The size of the <i>fontFamilyName</i> character array, in character count, including the terminated <b>NULL</b> character.  To find the size of <i>fontFamilyName</i>, use <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-getfontfamilynamelength">GetFontFamilyNameLength</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

