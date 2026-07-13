---
UID: NF:dwrite_3.IDWriteFontSet.FindFontFaceReference
title: IDWriteFontSet::FindFontFaceReference (dwrite_3.h)
description: Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations. (IDWriteFontSet.FindFontFaceReference)
helpviewer_keywords: ["FindFontFaceReference","FindFontFaceReference method [Direct Write]","FindFontFaceReference method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","FindFontFaceReference method","IDWriteFontSet.FindFontFaceReference","IDWriteFontSet::FindFontFaceReference","directwrite.idwritefontset_findfontfacereference","dwrite_3/IDWriteFontSet::FindFontFaceReference"]
old-location: directwrite\idwritefontset_findfontfacereference.htm
tech.root: DirectWrite
ms.assetid: dba55a36-8037-5564-59d8-e01189ff0020
ms.date: 09/10/2025
ms.keywords: FindFontFaceReference, FindFontFaceReference method [Direct Write], FindFontFaceReference method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],FindFontFaceReference method, IDWriteFontSet.FindFontFaceReference, IDWriteFontSet::FindFontFaceReference, directwrite.idwritefontset_findfontfacereference, dwrite_3/IDWriteFontSet::FindFontFaceReference
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
 - IDWriteFontSet::FindFontFaceReference
 - dwrite_3/IDWriteFontSet::FindFontFaceReference
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
 - IDWriteFontSet.FindFontFaceReference
---

# IDWriteFontSet::FindFontFaceReference


## -description

Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.

## -parameters

### -param fontFaceReference

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>*</b>

Font face object that specifies the physical font.

### -param listIndex [out]

Type: <b>UINT32*</b>

Receives the zero-based index of the matching font if the font was found, or UINT_MAX otherwise.

### -param exists [out]

Type: <b>BOOL*</b>

Receives TRUE if the font exists or FALSE otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>

