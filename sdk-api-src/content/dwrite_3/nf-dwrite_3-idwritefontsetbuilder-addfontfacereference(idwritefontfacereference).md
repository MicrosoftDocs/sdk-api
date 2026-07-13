---
UID: NF:dwrite_3.IDWriteFontSetBuilder.AddFontFaceReference(IDWriteFontFaceReference)
title: IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference) (dwrite_3.h)
description: Adds a reference to a font to the set being built. The necessary metadata will automatically be extracted from the font upon calling CreateFontSet. (overload 1/2)
helpviewer_keywords: ["AddFontFaceReference","AddFontFaceReference method [Direct Write]","AddFontFaceReference method [Direct Write]","IDWriteFontSetBuilder interface","IDWriteFontSetBuilder interface [Direct Write]","AddFontFaceReference method","IDWriteFontSetBuilder.AddFontFaceReference","IDWriteFontSetBuilder.AddFontFaceReference(IDWriteFontFaceReference)","IDWriteFontSetBuilder::AddFontFaceReference","IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference)","directwrite.idwritefontsetbuilder_addfontfacereference_1","dwrite_3/IDWriteFontSetBuilder::AddFontFaceReference"]
old-location: directwrite\idwritefontsetbuilder_addfontfacereference_1.htm
tech.root: DirectWrite
ms.assetid: 0E67F5EF-F8BB-47D9-995D-40879351DC17
ms.date: 09/10/2025
ms.keywords: AddFontFaceReference, AddFontFaceReference method [Direct Write], AddFontFaceReference method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],AddFontFaceReference method, IDWriteFontSetBuilder.AddFontFaceReference, IDWriteFontSetBuilder.AddFontFaceReference(IDWriteFontFaceReference), IDWriteFontSetBuilder::AddFontFaceReference, IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference), directwrite.idwritefontsetbuilder_addfontfacereference_1, dwrite_3/IDWriteFontSetBuilder::AddFontFaceReference
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
 - IDWriteFontSetBuilder::AddFontFaceReference
 - dwrite_3/IDWriteFontSetBuilder::AddFontFaceReference
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
 - IDWriteFontSetBuilder.AddFontFaceReference
---

# IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference)


## -description

Adds a reference to a font to the set being built. The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.

## -parameters

### -param fontFaceReference [in]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>*</b>

Font face reference object to add to the set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a>

