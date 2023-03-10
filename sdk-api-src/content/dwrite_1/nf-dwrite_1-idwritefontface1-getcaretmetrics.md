---
UID: NF:dwrite_1.IDWriteFontFace1.GetCaretMetrics
title: IDWriteFontFace1::GetCaretMetrics (dwrite_1.h)
description: Gets caret metrics for the font in design units.
helpviewer_keywords: ["GetCaretMetrics","GetCaretMetrics method [Direct Write]","GetCaretMetrics method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","GetCaretMetrics method","IDWriteFontFace1.GetCaretMetrics","IDWriteFontFace1::GetCaretMetrics","directwrite.idwritefontface1_getcaretmetrics","dwrite_1/IDWriteFontFace1::GetCaretMetrics"]
old-location: directwrite\idwritefontface1_getcaretmetrics.htm
tech.root: DirectWrite
ms.assetid: D9006617-A5B5-4575-9C00-26F52A73DC0D
ms.date: 12/05/2018
ms.keywords: GetCaretMetrics, GetCaretMetrics method [Direct Write], GetCaretMetrics method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetCaretMetrics method, IDWriteFontFace1.GetCaretMetrics, IDWriteFontFace1::GetCaretMetrics, directwrite.idwritefontface1_getcaretmetrics, dwrite_1/IDWriteFontFace1::GetCaretMetrics
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
 - IDWriteFontFace1::GetCaretMetrics
 - dwrite_1/IDWriteFontFace1::GetCaretMetrics
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
 - IDWriteFontFace1.GetCaretMetrics
---

# IDWriteFontFace1::GetCaretMetrics


## -description

Gets caret metrics for the font in design units.

## -parameters

### -param caretMetrics [out]

Type: <b>DWRITE_CARET_METRICS*</b>

A pointer to the <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics">DWRITE_CARET_METRICS</a> structure that is filled.

## -remarks

Caret metrics are used by
    text editors for drawing the correct caret placement and slant.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>

