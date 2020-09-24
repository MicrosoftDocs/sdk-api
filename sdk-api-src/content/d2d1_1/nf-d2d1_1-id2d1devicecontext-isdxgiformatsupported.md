---
UID: NF:d2d1_1.ID2D1DeviceContext.IsDxgiFormatSupported
title: ID2D1DeviceContext::IsDxgiFormatSupported (d2d1_1.h)
description: Indicates whether the format is supported by the device context.
helpviewer_keywords: ["ID2D1DeviceContext interface [Direct2D]","IsDxgiFormatSupported method","ID2D1DeviceContext.IsDxgiFormatSupported","ID2D1DeviceContext::IsDxgiFormatSupported","IsDxgiFormatSupported","IsDxgiFormatSupported method [Direct2D]","IsDxgiFormatSupported method [Direct2D]","ID2D1DeviceContext interface","d2d1_1/ID2D1DeviceContext::IsDxgiFormatSupported","direct2d.id2d1devicecontext_isdxgiformatsupported"]
old-location: direct2d\id2d1devicecontext_isdxgiformatsupported.htm
tech.root: Direct2D
ms.assetid: AA70292A-7B1C-4916-91CA-80263839BC3F
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],IsDxgiFormatSupported method, ID2D1DeviceContext.IsDxgiFormatSupported, ID2D1DeviceContext::IsDxgiFormatSupported, IsDxgiFormatSupported, IsDxgiFormatSupported method [Direct2D], IsDxgiFormatSupported method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::IsDxgiFormatSupported, direct2d.id2d1devicecontext_isdxgiformatsupported
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
 - ID2D1DeviceContext::IsDxgiFormatSupported
 - d2d1_1/ID2D1DeviceContext::IsDxgiFormatSupported
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
 - ID2D1DeviceContext.IsDxgiFormatSupported
---

# ID2D1DeviceContext::IsDxgiFormatSupported


## -description

 Indicates whether the format is supported by the device context.  The formats supported are usually determined by the underlying hardware.

## -parameters

### -param format

Type: <b>format</b>

The DXGI format to check.

## -returns

Type: <b>BOOL</b>

Returns TRUE if the format is supported.  Returns FALSE if the format is not supported.

## -remarks

You can use supported formats in the <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a> structure to create bitmaps and render targets.

Direct2D doesn't support all DXGI formats, even though they may have some level of Direct3D support by the hardware.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>