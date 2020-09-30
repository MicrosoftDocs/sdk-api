---
UID: NF:d2d1helper.RenderTargetProperties
title: RenderTargetProperties function (d2d1helper.h)
description: Creates a D2D1_RENDER_TARGET_PROPERTIES structure.
helpviewer_keywords: ["RenderTargetProperties","RenderTargetProperties function [Direct2D]","d2d1helper/RenderTargetProperties","direct2d.rendertargetproperties"]
old-location: direct2d\rendertargetproperties.htm
tech.root: Direct2D
ms.assetid: d384ff93-220f-4714-a76a-b8b495496d79
ms.date: 12/05/2018
ms.keywords: RenderTargetProperties, RenderTargetProperties function [Direct2D], d2d1helper/RenderTargetProperties, direct2d.rendertargetproperties
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
 - RenderTargetProperties
 - d2d1helper/RenderTargetProperties
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
 - RenderTargetProperties
---

# RenderTargetProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a> structure.

## -parameters

### -param type

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type">D2D1_RENDER_TARGET_TYPE</a></b>

A value that specifies whether the render target must use hardware rendering or software rendering. The default value, <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type">D2D1_RENDER_TARGET_TYPE_DEFAULT</a>, specifies that hardware rendering be used; if hardware rendering is not available, the render target uses software rendering. Note that WIC bitmap render targets do not support hardware rendering.

### -param pixelFormat [in]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

The pixel format and alpha mode of the render target. The default pixel format is <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat">D2D1::PixelFormat</a>, which tells Direct2D to select a pixel format that is supported by the render target.  For a list of pixel formats and alpha modes supported by each render target, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

### -param dpiX

Type: <b>FLOAT</b>

The horizontal DPI of the render target. The default value is 0.0. If both <i>dpiX</i> and <i>dpiY</i> are set to 0.0, the render target uses its default DPI.  For more information, see <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>.

### -param dpiY

Type: <b>FLOAT</b>

The vertical DPI of the render target. The default value is 0.0. If both <i>dpiX</i> and <i>dpiY</i> are set to 0.0, the render target uses its default DPI. For more information, see <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>.

### -param usage

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage">D2D1_RENDER_TARGET_USAGE</a></b>

Specifies how the render target is remotely rendered and whether it should be GDI-compatible.  The default value, <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage">D2D1_RENDER_TARGET_USAGE_NONE</a>, creates a render target that is not compatible with GDI and that uses Direct3D command-stream remote rendering, if it is available.

### -param minLevel

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_feature_level">D2D1_FEATURE_LEVEL</a></b>

The minimum Direct3D feature level that is required for hardware rendering. The default value, <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_feature_level">D2D1_FEATURE_LEVEL_DEFAULT</a>, indicates that Direct2D should determine whether the Direct3D feature level of the device is adequate. This field is used only when <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> and <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a> objects are created.  For more information, see <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a></b>

A <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a> that contains the specified settings.

## -see-also

<a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES Structure</a>



<a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>