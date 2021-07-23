---
UID: NF:dwrite.IDWriteTextLayout.GetOverhangMetrics
title: IDWriteTextLayout::GetOverhangMetrics (dwrite.h)
description: Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.
helpviewer_keywords: ["GetOverhangMetrics","GetOverhangMetrics method [Direct Write]","GetOverhangMetrics method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetOverhangMetrics method","IDWriteTextLayout.GetOverhangMetrics","IDWriteTextLayout::GetOverhangMetrics","directwrite.idwritetextlayout_getoverhangmetrics","dwrite/IDWriteTextLayout::GetOverhangMetrics"]
old-location: directwrite\idwritetextlayout_getoverhangmetrics.htm
tech.root: DirectWrite
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
ms.date: 12/05/2018
ms.keywords: GetOverhangMetrics, GetOverhangMetrics method [Direct Write], GetOverhangMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetOverhangMetrics method, IDWriteTextLayout.GetOverhangMetrics, IDWriteTextLayout::GetOverhangMetrics, directwrite.idwritetextlayout_getoverhangmetrics, dwrite/IDWriteTextLayout::GetOverhangMetrics
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteTextLayout::GetOverhangMetrics
 - dwrite/IDWriteTextLayout::GetOverhangMetrics
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
 - IDWriteTextLayout.GetOverhangMetrics
---

# IDWriteTextLayout::GetOverhangMetrics


## -description

Returns the overhangs (in DIPs) of the layout and all
    objects contained in it, including text glyphs and inline objects.

## -parameters

### -param overhangs [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics">DWRITE_OVERHANG_METRICS</a>*</b>

Overshoots of visible extents (in DIPs) outside the layout.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

