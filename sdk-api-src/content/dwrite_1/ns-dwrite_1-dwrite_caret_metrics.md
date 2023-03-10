---
UID: NS:dwrite_1.DWRITE_CARET_METRICS
title: DWRITE_CARET_METRICS (dwrite_1.h)
description: The DWRITE_CARET_METRICS structure specifies the metrics for caret placement in a font.
helpviewer_keywords: ["DWRITE_CARET_METRICS","DWRITE_CARET_METRICS structure [Direct Write]","directwrite.dwrite_caret_metrics","dwrite_1/DWRITE_CARET_METRICS"]
old-location: directwrite\dwrite_caret_metrics.htm
tech.root: DirectWrite
ms.assetid: CC7591F8-0671-436F-B0A7-C5D4C183D253
ms.date: 12/05/2018
ms.keywords: DWRITE_CARET_METRICS, DWRITE_CARET_METRICS structure [Direct Write], directwrite.dwrite_caret_metrics, dwrite_1/DWRITE_CARET_METRICS
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_CARET_METRICS
 - dwrite_1/DWRITE_CARET_METRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_CARET_METRICS
---

# DWRITE_CARET_METRICS structure


## -description

The <b>DWRITE_CARET_METRICS</b> structure specifies the metrics for caret placement in a font.

## -struct-fields

### -field slopeRise

Vertical rise of the caret in font design units. Rise / Run yields the caret angle. Rise = 1 for perfectly upright fonts (non-italic).

### -field slopeRun

Horizontal run of the caret in font design units. Rise / Run yields the caret angle. Run = 0 for perfectly upright fonts (non-italic).

### -field offset

Horizontal offset of the caret, in font design units, along the baseline for good appearance. Offset = 0 for perfectly upright fonts (non-italic).

## -see-also

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics">IDWriteFontFace1::GetCaretMetrics</a>

