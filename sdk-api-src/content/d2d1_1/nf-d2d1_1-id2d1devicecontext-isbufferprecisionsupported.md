---
UID: NF:d2d1_1.ID2D1DeviceContext.IsBufferPrecisionSupported
title: ID2D1DeviceContext::IsBufferPrecisionSupported (d2d1_1.h)
description: Indicates whether the buffer precision is supported by the underlying Direct3D device.
helpviewer_keywords: ["ID2D1DeviceContext interface [Direct2D]","IsBufferPrecisionSupported method","ID2D1DeviceContext.IsBufferPrecisionSupported","ID2D1DeviceContext::IsBufferPrecisionSupported","IsBufferPrecisionSupported","IsBufferPrecisionSupported method [Direct2D]","IsBufferPrecisionSupported method [Direct2D]","ID2D1DeviceContext interface","d2d1_1/ID2D1DeviceContext::IsBufferPrecisionSupported","direct2d.id2d1devicecontext_isbufferprecisionsupported"]
old-location: direct2d\id2d1devicecontext_isbufferprecisionsupported.htm
tech.root: Direct2D
ms.assetid: c65824dc-a9d5-4d4d-a2de-b4283153f64f
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],IsBufferPrecisionSupported method, ID2D1DeviceContext.IsBufferPrecisionSupported, ID2D1DeviceContext::IsBufferPrecisionSupported, IsBufferPrecisionSupported, IsBufferPrecisionSupported method [Direct2D], IsBufferPrecisionSupported method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::IsBufferPrecisionSupported, direct2d.id2d1devicecontext_isbufferprecisionsupported
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::IsBufferPrecisionSupported
 - d2d1_1/ID2D1DeviceContext::IsBufferPrecisionSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.IsBufferPrecisionSupported
---

# ID2D1DeviceContext::IsBufferPrecisionSupported


## -description

Indicates whether the buffer precision is supported by the underlying Direct3D <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">device.</a>

## -parameters

### -param bufferPrecision

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

The buffer precision to check.

## -returns

Type: <b>BOOL</b>

Returns TRUE if the buffer precision is supported.  Returns FALSE if the buffer precision is not supported.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>