---
UID: NF:dwrite_3.IDWriteFontSetBuilder.AddFontSet
title: IDWriteFontSetBuilder::AddFontSet (dwrite_3.h)
description: Appends an existing font set to the one being built, allowing one to aggregate two sets or to essentially extend an existing one.
helpviewer_keywords: ["AddFontSet","AddFontSet method [Direct Write]","AddFontSet method [Direct Write]","IDWriteFontSetBuilder interface","IDWriteFontSetBuilder interface [Direct Write]","AddFontSet method","IDWriteFontSetBuilder.AddFontSet","IDWriteFontSetBuilder::AddFontSet","directwrite.idwritefontsetbuilder_addfontset","dwrite_3/IDWriteFontSetBuilder::AddFontSet"]
old-location: directwrite\idwritefontsetbuilder_addfontset.htm
tech.root: DirectWrite
ms.assetid: F8B94A1B-905B-4A96-9943-12BB516311C2
ms.date: 12/05/2018
ms.keywords: AddFontSet, AddFontSet method [Direct Write], AddFontSet method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],AddFontSet method, IDWriteFontSetBuilder.AddFontSet, IDWriteFontSetBuilder::AddFontSet, directwrite.idwritefontsetbuilder_addfontset, dwrite_3/IDWriteFontSetBuilder::AddFontSet
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontSetBuilder::AddFontSet
 - dwrite_3/IDWriteFontSetBuilder::AddFontSet
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
 - IDWriteFontSetBuilder.AddFontSet
---

# IDWriteFontSetBuilder::AddFontSet


## -description

Appends an existing font set to the one being built, allowing
        one to aggregate two sets or to essentially extend an existing one.

## -parameters

### -param fontSet [in]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>*</b>

Font set to append font face references from.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a>

