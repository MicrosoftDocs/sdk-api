---
UID: NF:dwrite_2.IDWriteTextFormat1.SetOpticalAlignment
title: IDWriteTextFormat1::SetOpticalAlignment (dwrite_2.h)
description: Sets the optical margin alignment for the text format.
helpviewer_keywords: ["IDWriteTextFormat1 interface [Direct Write]","SetOpticalAlignment method","IDWriteTextFormat1.SetOpticalAlignment","IDWriteTextFormat1::SetOpticalAlignment","SetOpticalAlignment","SetOpticalAlignment method [Direct Write]","SetOpticalAlignment method [Direct Write]","IDWriteTextFormat1 interface","directwrite.idwritetextformat1_setopticalalignment","dwrite_2/IDWriteTextFormat1::SetOpticalAlignment"]
old-location: directwrite\idwritetextformat1_setopticalalignment.htm
tech.root: DirectWrite
ms.assetid: FA050DAC-2788-4159-B299-D4B6100D85F4
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat1 interface [Direct Write],SetOpticalAlignment method, IDWriteTextFormat1.SetOpticalAlignment, IDWriteTextFormat1::SetOpticalAlignment, SetOpticalAlignment, SetOpticalAlignment method [Direct Write], SetOpticalAlignment method [Direct Write],IDWriteTextFormat1 interface, directwrite.idwritetextformat1_setopticalalignment, dwrite_2/IDWriteTextFormat1::SetOpticalAlignment
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
 - IDWriteTextFormat1::SetOpticalAlignment
 - dwrite_2/IDWriteTextFormat1::SetOpticalAlignment
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
 - IDWriteTextFormat1.SetOpticalAlignment
---

# IDWriteTextFormat1::SetOpticalAlignment


## -description

Sets the optical margin alignment for the text format.

By default, glyphs are aligned to the margin by the default origin and side-bearings of the glyph. If you specify <b>DWRITE_OPTICAL_ALIGNMENT_USING_SIDE_BEARINGS</b>, then the alignment Suses the side bearings to offset the glyph from the aligned edge to ensure the ink of the glyphs are aligned.

## -parameters

### -param opticalAlignment

The optical alignment to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextformat1">IDWriteTextFormat1</a>

