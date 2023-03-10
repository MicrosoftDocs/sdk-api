---
UID: NS:dcommon.D2D1_PIXEL_FORMAT
title: D2D1_PIXEL_FORMAT (dcommon.h)
description: Contains the data format and alpha mode for a bitmap or render target.
helpviewer_keywords: ["D2D1_PIXEL_FORMAT","D2D1_PIXEL_FORMAT structure [Direct2D]","dcommon/D2D1_PIXEL_FORMAT","direct2d.D2D1_PIXEL_FORMAT"]
old-location: direct2d\D2D1_PIXEL_FORMAT.htm
tech.root: Direct2D
ms.assetid: e95afd9c-5793-4cb7-bcb8-aae4d28b6532
ms.date: 12/05/2018
ms.keywords: D2D1_PIXEL_FORMAT, D2D1_PIXEL_FORMAT structure [Direct2D], dcommon/D2D1_PIXEL_FORMAT, direct2d.D2D1_PIXEL_FORMAT
req.header: dcommon.h
req.include-header: D2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_PIXEL_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_PIXEL_FORMAT
 - dcommon/D2D1_PIXEL_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcommon.h
api_name:
 - D2D1_PIXEL_FORMAT
---

# D2D1_PIXEL_FORMAT structure


## -description

Contains the data format and alpha mode for a bitmap or render target.

## -struct-fields

### -field format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A value that specifies the size and arrangement of channels in each pixel.

### -field alphaMode

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE</a></b>

A value that specifies whether the alpha channel is using pre-multiplied alpha, straight alpha, whether it should be ignored and considered opaque, or whether it is unknown.

## -remarks

For more information about the pixel formats and alpha modes supported by each render target, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.


#### Examples

The following example creates a <b>D2D1_PIXEL_FORMAT</b> structure and uses it to specify the pixel format and alpha mode of an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>.


```cpp
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );


```

## -see-also

<a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat">D2D1::PixelFormat</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>