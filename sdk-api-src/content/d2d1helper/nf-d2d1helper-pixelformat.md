---
UID: NF:d2d1helper.PixelFormat
title: PixelFormat function (d2d1helper.h)
description: Creates a D2D1_PIXEL_FORMAT structure.
helpviewer_keywords: ["PixelFormat","PixelFormat function [Direct2D]","d2d1helper/PixelFormat","direct2d.pixelformat"]
old-location: direct2d\pixelformat.htm
tech.root: Direct2D
ms.assetid: 97128e07-68c2-40ab-bad1-7b6f599291b9
ms.date: 12/05/2018
ms.keywords: PixelFormat, PixelFormat function [Direct2D], d2d1helper/PixelFormat, direct2d.pixelformat
req.header: d2d1helper.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PixelFormat
 - d2d1helper/PixelFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - PixelFormat
---

# PixelFormat function


## -description

Creates a  <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a> structure.

## -parameters

### -param dxgiFormat [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A value that specifies the size and arrangement of channels in each pixel. The default value is <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKNOWN</a>.

### -param alphaMode [in]

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">ALPHA_MODE</a></b>

A value that specifies whether the alpha channel is using premultiplied alpha or  straight alpha, or whether it should be ignored and considered opaque. The default value is <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_UNKNOWN</a>.

## -returns

Type: <b><a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

A structure that  contains the data format and alpha mode for a bitmap or render target.

## -see-also

<a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>