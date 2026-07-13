---
UID: NF:dwrite_3.IDWriteColorGlyphRunEnumerator1.GetCurrentRun
title: IDWriteColorGlyphRunEnumerator1::GetCurrentRun (dwrite_3.h)
description: Gets the current color glyph run.
helpviewer_keywords: ["GetCurrentRun","GetCurrentRun method [Direct Write]","GetCurrentRun method [Direct Write]","IDWriteColorGlyphRunEnumerator1 interface","IDWriteColorGlyphRunEnumerator1 interface [Direct Write]","GetCurrentRun method","IDWriteColorGlyphRunEnumerator1.GetCurrentRun","IDWriteColorGlyphRunEnumerator1::GetCurrentRun","directwrite.idwritecolorglyphrunenumerator1_getcurrentrun","dwrite_3/IDWriteColorGlyphRunEnumerator1::GetCurrentRun"]
old-location: directwrite\idwritecolorglyphrunenumerator1_getcurrentrun.htm
tech.root: DirectWrite
ms.assetid: 0FEFD8EB-20E7-4E04-9C31-1A763D2FB816
ms.date: 09/10/2025
ms.keywords: GetCurrentRun, GetCurrentRun method [Direct Write], GetCurrentRun method [Direct Write],IDWriteColorGlyphRunEnumerator1 interface, IDWriteColorGlyphRunEnumerator1 interface [Direct Write],GetCurrentRun method, IDWriteColorGlyphRunEnumerator1.GetCurrentRun, IDWriteColorGlyphRunEnumerator1::GetCurrentRun, directwrite.idwritecolorglyphrunenumerator1_getcurrentrun, dwrite_3/IDWriteColorGlyphRunEnumerator1::GetCurrentRun
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 14393
req.target-min-winversvr: Windows 10 Build 14393
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteColorGlyphRunEnumerator1::GetCurrentRun
 - dwrite_3/IDWriteColorGlyphRunEnumerator1::GetCurrentRun
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteColorGlyphRunEnumerator1.GetCurrentRun
---

# IDWriteColorGlyphRunEnumerator1::GetCurrentRun


## -description

Gets the current color glyph run.

## -parameters

### -param colorGlyphRun [out]

Type: <b><a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1">DWRITE_COLOR_GLYPH_RUN1</a></b>

Receives a pointer to the color glyph run. The pointer remains valid until the next call to
          MoveNext or until the interface is released.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Standard HRESULT error code. An error is returned if there is
          no current glyph run, i.e., if MoveNext has not yet been called
          or if the end of the sequence has been reached.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1">IDWriteColorGlyphRunEnumerator1</a>

