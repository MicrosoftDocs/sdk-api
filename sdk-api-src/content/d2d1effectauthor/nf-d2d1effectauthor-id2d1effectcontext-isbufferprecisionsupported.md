---
UID: NF:d2d1effectauthor.ID2D1EffectContext.IsBufferPrecisionSupported
title: ID2D1EffectContext::IsBufferPrecisionSupported (d2d1effectauthor.h)
description: Indicates whether the buffer precision is supported by the underlying Direct2D device.
helpviewer_keywords: ["ID2D1EffectContext interface [Direct2D]","IsBufferPrecisionSupported method","ID2D1EffectContext.IsBufferPrecisionSupported","ID2D1EffectContext::IsBufferPrecisionSupported","IsBufferPrecisionSupported","IsBufferPrecisionSupported method [Direct2D]","IsBufferPrecisionSupported method [Direct2D]","ID2D1EffectContext interface","d2d1effectauthor/ID2D1EffectContext::IsBufferPrecisionSupported","direct2d.id2d1effectcontext_isbufferprecisionsupported"]
old-location: direct2d\id2d1effectcontext_isbufferprecisionsupported.htm
tech.root: Direct2D
ms.assetid: 731A7CF3-03E7-4D38-A8DD-8D207AE90B16
ms.date: 12/05/2018
ms.keywords: ID2D1EffectContext interface [Direct2D],IsBufferPrecisionSupported method, ID2D1EffectContext.IsBufferPrecisionSupported, ID2D1EffectContext::IsBufferPrecisionSupported, IsBufferPrecisionSupported, IsBufferPrecisionSupported method [Direct2D], IsBufferPrecisionSupported method [Direct2D],ID2D1EffectContext interface, d2d1effectauthor/ID2D1EffectContext::IsBufferPrecisionSupported, direct2d.id2d1effectcontext_isbufferprecisionsupported
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::IsBufferPrecisionSupported
 - d2d1effectauthor/ID2D1EffectContext::IsBufferPrecisionSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1EffectContext.IsBufferPrecisionSupported
---

# ID2D1EffectContext::IsBufferPrecisionSupported


## -description

 Indicates whether the buffer precision is supported by the underlying Direct2D <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">device.</a>

## -parameters

### -param bufferPrecision

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

The buffer precision to check.

## -returns

Type: <b>BOOL</b>

Returns TRUE if the buffer precision is supported.  Returns FALSE if the buffer precision is not supported.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>