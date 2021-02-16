---
UID: NF:dwrite_1.IDWriteFontFace1.GetUnicodeRanges
title: IDWriteFontFace1::GetUnicodeRanges (dwrite_1.h)
description: Retrieves a list of character ranges supported by a font.
helpviewer_keywords: ["GetUnicodeRanges","GetUnicodeRanges method [Direct Write]","GetUnicodeRanges method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","GetUnicodeRanges method","IDWriteFontFace1.GetUnicodeRanges","IDWriteFontFace1::GetUnicodeRanges","directwrite.idwritefontface1_getunicoderanges","dwrite_1/IDWriteFontFace1::GetUnicodeRanges"]
old-location: directwrite\idwritefontface1_getunicoderanges.htm
tech.root: DirectWrite
ms.assetid: 0464BA91-B098-463D-A4A9-8D3C05E45F0E
ms.date: 12/05/2018
ms.keywords: GetUnicodeRanges, GetUnicodeRanges method [Direct Write], GetUnicodeRanges method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetUnicodeRanges method, IDWriteFontFace1.GetUnicodeRanges, IDWriteFontFace1::GetUnicodeRanges, directwrite.idwritefontface1_getunicoderanges, dwrite_1/IDWriteFontFace1::GetUnicodeRanges
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace1::GetUnicodeRanges
 - dwrite_1/IDWriteFontFace1::GetUnicodeRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.GetUnicodeRanges
---

# IDWriteFontFace1::GetUnicodeRanges


## -description

Retrieves a list of character ranges supported by a font.

## -parameters

### -param maxRangeCount

Type: <b>UINT32</b>

Maximum number of character ranges passed
    in from the client.

### -param unicodeRanges [out, optional]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range">DWRITE_UNICODE_RANGE</a>*</b>

An array of <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range">DWRITE_UNICODE_RANGE</a> structures that are filled with the character ranges.

### -param actualRangeCount [out]

Type: <b>UINT32*</b>

A pointer to the actual number of character ranges,
    regardless of the maximum count.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method executed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_NOT_SUFFICIENT_BUFFER</dt>
</dl>
</td>
<td width="60%">
The buffer is too small.  The <i>actualRangeCount</i> was more than the <i>maxRangeCount</i>.

</td>
</tr>
</table>

## -remarks

A 
  list of character ranges supported by the font is
    useful for scenarios like character picking, glyph display, and
    efficient font selection lookup. This is similar to GDI's
    <a href="/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges">GetFontUnicodeRanges</a>, except that it returns the full Unicode range,
    not just 16-bit UCS-2.

These ranges are from the cmap, not the OS/2::ulCodePageRange1.

If this method is unavailable, you can use the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices">IDWriteFontFace::GetGlyphIndices</a> method to check for missing glyphs.  The method returns the 0 index for glyphs that aren't present in the font.

 The <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-hascharacter">IDWriteFont::HasCharacter</a> method is often simpler in cases where you need to check a single character or a series of single characters in succession, such as in font fallback.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>

