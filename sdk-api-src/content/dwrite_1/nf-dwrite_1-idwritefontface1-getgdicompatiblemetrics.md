---
UID: NF:dwrite_1.IDWriteFontFace1.GetGdiCompatibleMetrics
title: IDWriteFontFace1::GetGdiCompatibleMetrics (dwrite_1.h)
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations. (IDWriteFontFace1.GetGdiCompatibleMetrics)
helpviewer_keywords: ["GetGdiCompatibleMetrics","GetGdiCompatibleMetrics method [Direct Write]","GetGdiCompatibleMetrics method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","GetGdiCompatibleMetrics method","IDWriteFontFace1.GetGdiCompatibleMetrics","IDWriteFontFace1::GetGdiCompatibleMetrics","directwrite.idwritefontface1_getgdicompatiblemetrics","dwrite_1/IDWriteFontFace1::GetGdiCompatibleMetrics"]
old-location: directwrite\idwritefontface1_getgdicompatiblemetrics.htm
tech.root: DirectWrite
ms.assetid: 2FD26970-8CF3-453F-A08D-30CC4A820281
ms.date: 12/05/2018
ms.keywords: GetGdiCompatibleMetrics, GetGdiCompatibleMetrics method [Direct Write], GetGdiCompatibleMetrics method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetGdiCompatibleMetrics method, IDWriteFontFace1.GetGdiCompatibleMetrics, IDWriteFontFace1::GetGdiCompatibleMetrics, directwrite.idwritefontface1_getgdicompatiblemetrics, dwrite_1/IDWriteFontFace1::GetGdiCompatibleMetrics
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
 - IDWriteFontFace1::GetGdiCompatibleMetrics
 - dwrite_1/IDWriteFontFace1::GetGdiCompatibleMetrics
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
 - IDWriteFontFace1.GetGdiCompatibleMetrics
---

# IDWriteFontFace1::GetGdiCompatibleMetrics


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

### -param fontMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1">DWRITE_FONT_METRICS1</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1">DWRITE_FONT_METRICS1</a> structure to fill in. The metrics returned by this function are in font design units.

## -returns

Type: <b>HRESULT</b>

Standard HRESULT error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>



<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>

