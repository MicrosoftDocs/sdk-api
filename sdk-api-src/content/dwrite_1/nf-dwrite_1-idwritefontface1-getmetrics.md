---
UID: NF:dwrite_1.IDWriteFontFace1.GetMetrics
title: IDWriteFontFace1::GetMetrics (dwrite_1.h)
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations. (IDWriteFontFace1.GetMetrics)
helpviewer_keywords: ["GetMetrics","GetMetrics method [Direct Write]","GetMetrics method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","GetMetrics method","IDWriteFontFace1.GetMetrics","IDWriteFontFace1::GetMetrics","directwrite.idwritefontface1_getmetrics","dwrite_1/IDWriteFontFace1::GetMetrics"]
old-location: directwrite\idwritefontface1_getmetrics.htm
tech.root: DirectWrite
ms.assetid: 7F899D56-F56B-4C4C-A17D-B42A34CAA0F1
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetMetrics method, IDWriteFontFace1.GetMetrics, IDWriteFontFace1::GetMetrics, directwrite.idwritefontface1_getmetrics, dwrite_1/IDWriteFontFace1::GetMetrics
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
 - IDWriteFontFace1::GetMetrics
 - dwrite_1/IDWriteFontFace1::GetMetrics
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
 - IDWriteFontFace1.GetMetrics
---

# IDWriteFontFace1::GetMetrics


## -description

 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

## -parameters

### -param fontMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1">DWRITE_FONT_METRICS1</a>*</b>

A filled <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1">DWRITE_FONT_METRICS1</a> structure that holds metrics for the current font face element.
     The metrics returned by this method are in font design units.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>

