---
UID: NF:dwrite_3.IDWriteFontSetBuilder.CreateFontSet
title: IDWriteFontSetBuilder::CreateFontSet (dwrite_3.h)
description: Creates a font set from all the font face references added so far with AddFontFaceReference.
helpviewer_keywords: ["CreateFontSet","CreateFontSet method [Direct Write]","CreateFontSet method [Direct Write]","IDWriteFontSetBuilder interface","IDWriteFontSetBuilder interface [Direct Write]","CreateFontSet method","IDWriteFontSetBuilder.CreateFontSet","IDWriteFontSetBuilder::CreateFontSet","directwrite.idwritefontsetbuilder_createfontset","dwrite_3/IDWriteFontSetBuilder::CreateFontSet"]
old-location: directwrite\idwritefontsetbuilder_createfontset.htm
tech.root: DirectWrite
ms.assetid: 58923F9C-4DAA-4F97-AE25-A2560176E0F2
ms.date: 12/05/2018
ms.keywords: CreateFontSet, CreateFontSet method [Direct Write], CreateFontSet method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],CreateFontSet method, IDWriteFontSetBuilder.CreateFontSet, IDWriteFontSetBuilder::CreateFontSet, directwrite.idwritefontsetbuilder_createfontset, dwrite_3/IDWriteFontSetBuilder::CreateFontSet
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
 - IDWriteFontSetBuilder::CreateFontSet
 - dwrite_3/IDWriteFontSetBuilder::CreateFontSet
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
 - IDWriteFontSetBuilder.CreateFontSet
---

# IDWriteFontSetBuilder::CreateFontSet


## -description

Creates a font set from all the font face references added so
        far with AddFontFaceReference.

## -parameters

### -param fontSet [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>**</b>

Contains the newly created font set object, or nullptr in case of failure.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creating a font set takes less time if the references were added with metadata rather than needing to extract the metadata from the
      font file.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a>

