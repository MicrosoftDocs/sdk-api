---
UID: NF:dwrite.IDWriteFontFace.GetGlyphIndices
title: IDWriteFontFace::GetGlyphIndices (dwrite.h)
description: Returns the nominal mapping of UCS4 Unicode code points to glyph indices as defined by the font 'CMAP' table.
helpviewer_keywords: ["GetGlyphIndices","GetGlyphIndices method [Direct Write]","GetGlyphIndices method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetGlyphIndices method","IDWriteFontFace.GetGlyphIndices","IDWriteFontFace::GetGlyphIndices","directwrite.IDWriteFontFace_GetGlyphIndices","dwrite/IDWriteFontFace::GetGlyphIndices"]
old-location: directwrite\IDWriteFontFace_GetGlyphIndices.htm
tech.root: DirectWrite
ms.assetid: 2dbaec8c-464e-45a5-b420-fa1ec3d224bd
ms.date: 12/05/2018
ms.keywords: GetGlyphIndices, GetGlyphIndices method [Direct Write], GetGlyphIndices method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetGlyphIndices method, IDWriteFontFace.GetGlyphIndices, IDWriteFontFace::GetGlyphIndices, directwrite.IDWriteFontFace_GetGlyphIndices, dwrite/IDWriteFontFace::GetGlyphIndices
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
 - IDWriteFontFace::GetGlyphIndices
 - dwrite/IDWriteFontFace::GetGlyphIndices
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
 - IDWriteFontFace.GetGlyphIndices
---

# IDWriteFontFace::GetGlyphIndices


## -description

 Returns the nominal mapping of UCS4 Unicode code points to glyph indices as defined by the font 'CMAP' table.

## -parameters

### -param codePoints [in]

Type: <b>const UINT32*</b>

An array of USC4 code points from which to obtain nominal glyph indices. The array must be allocated and be able to contain the number of elements specified by <i>codePointCount</i>.

### -param codePointCount

Type: <b>UINT32</b>

The number of elements in the <i>codePoints</i> array.

### -param glyphIndices [out]

Type: <b>UINT16*</b>

When this method returns, contains a pointer to an array of nominal glyph indices filled by this function.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Note that this mapping is primarily provided for line layout engines built on top of the physical font API.
     Because of OpenType glyph substitution and line layout character substitution, the nominal conversion does not always correspond
     to how a Unicode string will map to glyph indices when rendering using a particular font face.
     Also, note that Unicode variant selectors provide for alternate mappings for character to glyph.
     This call will always return the default variant.

 When characters are not present in the font this method returns the index 0, which is the undefined glyph or ".notdef" glyph.  If a character isn't in a font, IDWriteFont::HasCharacter returns false and GetUnicodeRanges doesn't return it in the range.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

