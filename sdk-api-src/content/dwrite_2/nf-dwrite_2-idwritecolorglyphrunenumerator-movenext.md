---
UID: NF:dwrite_2.IDWriteColorGlyphRunEnumerator.MoveNext
title: IDWriteColorGlyphRunEnumerator::MoveNext (dwrite_2.h)
description: Move to the next glyph run in the enumerator.
helpviewer_keywords: ["IDWriteColorGlyphRunEnumerator interface [Direct Write]","MoveNext method","IDWriteColorGlyphRunEnumerator.MoveNext","IDWriteColorGlyphRunEnumerator::MoveNext","MoveNext","MoveNext method [Direct Write]","MoveNext method [Direct Write]","IDWriteColorGlyphRunEnumerator interface","directwrite.idwritecolorglyphrunenumerator_movenext","dwrite_2/IDWriteColorGlyphRunEnumerator::MoveNext"]
old-location: directwrite\idwritecolorglyphrunenumerator_movenext.htm
tech.root: DirectWrite
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
ms.date: 12/05/2018
ms.keywords: IDWriteColorGlyphRunEnumerator interface [Direct Write],MoveNext method, IDWriteColorGlyphRunEnumerator.MoveNext, IDWriteColorGlyphRunEnumerator::MoveNext, MoveNext, MoveNext method [Direct Write], MoveNext method [Direct Write],IDWriteColorGlyphRunEnumerator interface, directwrite.idwritecolorglyphrunenumerator_movenext, dwrite_2/IDWriteColorGlyphRunEnumerator::MoveNext
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteColorGlyphRunEnumerator::MoveNext
 - dwrite_2/IDWriteColorGlyphRunEnumerator::MoveNext
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
 - IDWriteColorGlyphRunEnumerator.MoveNext
---

# IDWriteColorGlyphRunEnumerator::MoveNext


## -description

Move to the next glyph run in the enumerator.

## -parameters

### -param hasRun [out]

Type: <b>BOOL*</b>

Returns <b>TRUE</b> if there is a next glyph run.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritecolorglyphrunenumerator">IDWriteColorGlyphRunEnumerator</a>

