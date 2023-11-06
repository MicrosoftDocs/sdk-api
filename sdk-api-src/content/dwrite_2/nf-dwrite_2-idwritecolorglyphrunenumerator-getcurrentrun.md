---
UID: NF:dwrite_2.IDWriteColorGlyphRunEnumerator.GetCurrentRun
title: IDWriteColorGlyphRunEnumerator::GetCurrentRun (dwrite_2.h)
description: Returns the current glyph run of the enumerator.
helpviewer_keywords: ["GetCurrentRun","GetCurrentRun method [Direct Write]","GetCurrentRun method [Direct Write]","IDWriteColorGlyphRunEnumerator interface","IDWriteColorGlyphRunEnumerator interface [Direct Write]","GetCurrentRun method","IDWriteColorGlyphRunEnumerator.GetCurrentRun","IDWriteColorGlyphRunEnumerator::GetCurrentRun","directwrite.idwritecolorglyphrunenumerator_getcurrentrun","dwrite_2/IDWriteColorGlyphRunEnumerator::GetCurrentRun"]
old-location: directwrite\idwritecolorglyphrunenumerator_getcurrentrun.htm
tech.root: DirectWrite
ms.assetid: F4D89E35-3846-41F0-A724-3648DC9D487E
ms.date: 12/05/2018
ms.keywords: GetCurrentRun, GetCurrentRun method [Direct Write], GetCurrentRun method [Direct Write],IDWriteColorGlyphRunEnumerator interface, IDWriteColorGlyphRunEnumerator interface [Direct Write],GetCurrentRun method, IDWriteColorGlyphRunEnumerator.GetCurrentRun, IDWriteColorGlyphRunEnumerator::GetCurrentRun, directwrite.idwritecolorglyphrunenumerator_getcurrentrun, dwrite_2/IDWriteColorGlyphRunEnumerator::GetCurrentRun
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
 - IDWriteColorGlyphRunEnumerator::GetCurrentRun
 - dwrite_2/IDWriteColorGlyphRunEnumerator::GetCurrentRun
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
 - IDWriteColorGlyphRunEnumerator.GetCurrentRun
---

# IDWriteColorGlyphRunEnumerator::GetCurrentRun


## -description

Returns the current glyph run of the enumerator.

## -parameters

### -param colorGlyphRun [out]

Type: <b>const <a href="/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_color_glyph_run">DWRITE_COLOR_GLYPH_RUN</a>**</b>

A pointer to the current glyph run.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritecolorglyphrunenumerator">IDWriteColorGlyphRunEnumerator</a>

