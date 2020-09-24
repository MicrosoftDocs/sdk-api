---
UID: NS:wincodec.WICDdsFormatInfo
title: WICDdsFormatInfo (wincodec.h)
description: Specifies the DXGI_FORMAT and block information of a DDS format.
helpviewer_keywords: ["PWICDdsFormatInfo","PWICDdsFormatInfo structure pointer [Windows Imaging Component]","WICDdsFormatInfo","WICDdsFormatInfo structure [Windows Imaging Component]","wic.wicddsformatinfo","wincodec/PWICDdsFormatInfo","wincodec/WICDdsFormatInfo"]
old-location: wic\wicddsformatinfo.htm
tech.root: wic
ms.assetid: C5F1DA49-EC11-4068-9DC6-D721894371F9
ms.date: 12/05/2018
ms.keywords: PWICDdsFormatInfo, PWICDdsFormatInfo structure pointer [Windows Imaging Component], WICDdsFormatInfo, WICDdsFormatInfo structure [Windows Imaging Component], wic.wicddsformatinfo, wincodec/PWICDdsFormatInfo, wincodec/WICDdsFormatInfo
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICDdsFormatInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICDdsFormatInfo
 - wincodec/WICDdsFormatInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICDdsFormatInfo
---

# WICDdsFormatInfo structure


## -description

Specifies the <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> and block information of a DDS format.

## -struct-fields

### -field DxgiFormat

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>

### -field BytesPerBlock

Type: <b>UINT</b>

The size of a single block in bytes. For <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> values that are not block-based, the value is equal to the size of a single pixel in bytes.

### -field BlockWidth

Type: <b>UINT</b>

The width of a single block in pixels. For <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> values that are not block-based, the value is 1.

### -field BlockHeight

Type: <b>UINT</b>

The height of a single block in pixels. For <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> values that are not block-based, the value is 1.

## -see-also

<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>