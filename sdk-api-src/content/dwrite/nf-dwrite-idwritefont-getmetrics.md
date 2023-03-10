---
UID: NF:dwrite.IDWriteFont.GetMetrics
title: IDWriteFont::GetMetrics (dwrite.h)
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations. (IDWriteFont.GetMetrics)
helpviewer_keywords: ["GetMetrics","GetMetrics method [Direct Write]","GetMetrics method [Direct Write]","IDWriteFont interface","IDWriteFont interface [Direct Write]","GetMetrics method","IDWriteFont.GetMetrics","IDWriteFont::GetMetrics","directwrite.IDWriteFont_GetMetrics","dwrite/IDWriteFont::GetMetrics"]
old-location: directwrite\IDWriteFont_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: 0634d683-2c6e-40cb-94d9-2cf128fc3421
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetMetrics method, IDWriteFont.GetMetrics, IDWriteFont::GetMetrics, directwrite.IDWriteFont_GetMetrics, dwrite/IDWriteFont::GetMetrics
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
 - IDWriteFont::GetMetrics
 - dwrite/IDWriteFont::GetMetrics
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
 - IDWriteFont.GetMetrics
---

# IDWriteFont::GetMetrics


## -description

 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

## -parameters

### -param fontMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a>*</b>

When this method returns, contains a structure that has font metrics for the current font face. The metrics returned by this function are in font design units.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>

