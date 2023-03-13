---
UID: NF:dwrite_1.IDWriteFont1.GetMetrics
title: IDWriteFont1::GetMetrics (dwrite_1.h)
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations. (IDWriteFont1.GetMetrics)
helpviewer_keywords: ["GetMetrics","GetMetrics method [Direct Write]","GetMetrics method [Direct Write]","IDWriteFont1 interface","IDWriteFont1 interface [Direct Write]","GetMetrics method","IDWriteFont1.GetMetrics","IDWriteFont1::GetMetrics","directwrite.idwritefont1_getmetrics","dwrite_1/IDWriteFont1::GetMetrics"]
old-location: directwrite\idwritefont1_getmetrics.htm
tech.root: DirectWrite
ms.assetid: 2D8D22B9-3F5B-4257-8D74-699C4040C9DB
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteFont1 interface, IDWriteFont1 interface [Direct Write],GetMetrics method, IDWriteFont1.GetMetrics, IDWriteFont1::GetMetrics, directwrite.idwritefont1_getmetrics, dwrite_1/IDWriteFont1::GetMetrics
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
 - IDWriteFont1::GetMetrics
 - dwrite_1/IDWriteFont1::GetMetrics
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
 - IDWriteFont1.GetMetrics
---

# IDWriteFont1::GetMetrics


## -description

 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

## -parameters

### -param fontMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1">DWRITE_FONT_METRICS1</a>*</b>

 A filled  <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1">DWRITE_FONT_METRICS1</a> structure that has font metrics for the current font face. The metrics returned by this method are in font design units.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1">IDWriteFont1</a>

