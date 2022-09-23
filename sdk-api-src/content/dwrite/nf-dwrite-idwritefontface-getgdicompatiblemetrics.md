---
UID: NF:dwrite.IDWriteFontFace.GetGdiCompatibleMetrics
title: IDWriteFontFace::GetGdiCompatibleMetrics (dwrite.h)
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations. (IDWriteFontFace.GetGdiCompatibleMetrics)
helpviewer_keywords: ["GetGdiCompatibleMetrics","GetGdiCompatibleMetrics method [Direct Write]","GetGdiCompatibleMetrics method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetGdiCompatibleMetrics method","IDWriteFontFace.GetGdiCompatibleMetrics","IDWriteFontFace::GetGdiCompatibleMetrics","directwrite.idwritefontface_getgdicompatiblemetrics","dwrite/IDWriteFontFace::GetGdiCompatibleMetrics"]
old-location: directwrite\idwritefontface_getgdicompatiblemetrics.htm
tech.root: DirectWrite
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
ms.date: 12/05/2018
ms.keywords: GetGdiCompatibleMetrics, GetGdiCompatibleMetrics method [Direct Write], GetGdiCompatibleMetrics method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetGdiCompatibleMetrics method, IDWriteFontFace.GetGdiCompatibleMetrics, IDWriteFontFace::GetGdiCompatibleMetrics, directwrite.idwritefontface_getgdicompatiblemetrics, dwrite/IDWriteFontFace::GetGdiCompatibleMetrics
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
 - IDWriteFontFace::GetGdiCompatibleMetrics
 - dwrite/IDWriteFontFace::GetGdiCompatibleMetrics
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
 - IDWriteFontFace.GetGdiCompatibleMetrics
---

# IDWriteFontFace::GetGdiCompatibleMetrics


## -description

Obtains design units and common metrics for the font face.
    These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.

## -parameters

### -param emSize

Type: <b>FLOAT</b>

The logical size of the font in DIP units.

### -param pixelsPerDip

Type: <b>FLOAT</b>

The number of physical pixels per DIP.

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

An optional transform applied to the glyphs and their positions. This transform is applied after the scaling specified by the font size and <i>pixelsPerDip</i>.

### -param fontFaceMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRIC</a>S structure to fill in. The metrics returned by this function are in font design units.

## -returns

Type: <b>HRESULT</b>

Standard HRESULT error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

