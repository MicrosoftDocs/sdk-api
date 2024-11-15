---
UID: NF:dwrite_3.IDWriteFontCollection1.GetFontSet
title: IDWriteFontCollection1::GetFontSet (dwrite_3.h)
description: Gets the underlying font set used by this collection.
helpviewer_keywords: ["GetFontSet","GetFontSet method [Direct Write]","GetFontSet method [Direct Write]","IDWriteFontCollection1 interface","IDWriteFontCollection1 interface [Direct Write]","GetFontSet method","IDWriteFontCollection1.GetFontSet","IDWriteFontCollection1::GetFontSet","directwrite.idwritefontcollection1_getfontset","dwrite_3/IDWriteFontCollection1::GetFontSet"]
old-location: directwrite\idwritefontcollection1_getfontset.htm
tech.root: DirectWrite
ms.assetid: 964732b9-bf0f-2ec8-d566-3fa06c9d57e4
ms.date: 12/05/2018
ms.keywords: GetFontSet, GetFontSet method [Direct Write], GetFontSet method [Direct Write],IDWriteFontCollection1 interface, IDWriteFontCollection1 interface [Direct Write],GetFontSet method, IDWriteFontCollection1.GetFontSet, IDWriteFontCollection1::GetFontSet, directwrite.idwritefontcollection1_getfontset, dwrite_3/IDWriteFontCollection1::GetFontSet
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
 - IDWriteFontCollection1::GetFontSet
 - dwrite_3/IDWriteFontCollection1::GetFontSet
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
 - IDWriteFontCollection1.GetFontSet
---

# IDWriteFontCollection1::GetFontSet


## -description

Gets the underlying font set used by this collection.

## -parameters

### -param fontSet [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>**</b>

Returns the font set used by the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1">IDWriteFontCollection1</a>

