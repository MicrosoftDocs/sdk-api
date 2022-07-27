---
UID: NF:dwrite.IDWriteFontFace.GetMetrics
title: IDWriteFontFace::GetMetrics (dwrite.h)
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations. (IDWriteFontFace.GetMetrics)
helpviewer_keywords: ["GetMetrics","GetMetrics method [Direct Write]","GetMetrics method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetMetrics method","IDWriteFontFace.GetMetrics","IDWriteFontFace::GetMetrics","directwrite.IDWriteFontFace_GetMetrics","dwrite/IDWriteFontFace::GetMetrics"]
old-location: directwrite\IDWriteFontFace_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: 09271b06-71cb-4702-861f-c3f6b9069c15
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetMetrics method, IDWriteFontFace.GetMetrics, IDWriteFontFace::GetMetrics, directwrite.IDWriteFontFace_GetMetrics, dwrite/IDWriteFontFace::GetMetrics
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
 - IDWriteFontFace::GetMetrics
 - dwrite/IDWriteFontFace::GetMetrics
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
 - IDWriteFontFace.GetMetrics
---

# IDWriteFontFace::GetMetrics


## -description

 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

## -parameters

### -param fontFaceMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a>*</b>

When this method returns, a <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a> structure that holds metrics (such as ascent, descent, or cap height) for the current font face element.
     The metrics returned by this function are in font design units.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

