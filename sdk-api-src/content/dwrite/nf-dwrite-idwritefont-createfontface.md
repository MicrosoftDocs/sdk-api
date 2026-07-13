---
UID: NF:dwrite.IDWriteFont.CreateFontFace
title: IDWriteFont::CreateFontFace (dwrite.h)
description: Creates a font face object for the font. (IDWriteFont.CreateFontFace)
helpviewer_keywords: ["CreateFontFace","CreateFontFace method [Direct Write]","CreateFontFace method [Direct Write]","IDWriteFont interface","IDWriteFont interface [Direct Write]","CreateFontFace method","IDWriteFont.CreateFontFace","IDWriteFont::CreateFontFace","directwrite.IDWriteFont_CreateFontFace","dwrite/IDWriteFont::CreateFontFace"]
old-location: directwrite\IDWriteFont_CreateFontFace.htm
tech.root: DirectWrite
ms.assetid: dd70a9f7-43f3-43e9-94d9-fe70b1b53f59
ms.date: 12/05/2018
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],CreateFontFace method, IDWriteFont.CreateFontFace, IDWriteFont::CreateFontFace, directwrite.IDWriteFont_CreateFontFace, dwrite/IDWriteFont::CreateFontFace
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
 - IDWriteFont::CreateFontFace
 - dwrite/IDWriteFont::CreateFontFace
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
 - IDWriteFont.CreateFontFace
---

# IDWriteFont::CreateFontFace


## -description

 Creates a font face object for the font.

## -parameters

### -param fontFace [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>**</b>

When this method returns, contains an address of a pointer to the newly created font face object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>

