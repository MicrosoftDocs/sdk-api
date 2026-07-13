---
UID: NS:d2d1.D2D1_RENDER_TARGET_PROPERTIES
title: D2D1_RENDER_TARGET_PROPERTIES (d2d1.h)
description: Contains rendering options (hardware or software), pixel format, DPI information, remoting options, and Direct3D support requirements for a render target.
helpviewer_keywords: ["D2D1_RENDER_TARGET_PROPERTIES","D2D1_RENDER_TARGET_PROPERTIES structure [Direct2D]","d2d1/D2D1_RENDER_TARGET_PROPERTIES","direct2d.D2D1_RENDER_TARGET_PROPERTIES"]
old-location: direct2d\D2D1_RENDER_TARGET_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: 360900bd-1353-4a92-865c-ad34d5e98123
ms.date: 12/05/2018
ms.keywords: D2D1_RENDER_TARGET_PROPERTIES, D2D1_RENDER_TARGET_PROPERTIES structure [Direct2D], d2d1/D2D1_RENDER_TARGET_PROPERTIES, direct2d.D2D1_RENDER_TARGET_PROPERTIES
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_RENDER_TARGET_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_RENDER_TARGET_PROPERTIES
 - d2d1/D2D1_RENDER_TARGET_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_RENDER_TARGET_PROPERTIES
---

# D2D1_RENDER_TARGET_PROPERTIES structure


## -description

Contains rendering options (hardware or software), pixel format, DPI information, remoting options, and Direct3D support requirements for a render target.

## -struct-fields

### -field type

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_type">D2D1_RENDER_TARGET_TYPE</a></b>

A value that specifies whether the render target should force hardware or software rendering. A value of <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_type">D2D1_RENDER_TARGET_TYPE_DEFAULT</a> specifies that the render target should use hardware rendering if it is available; otherwise, it uses software rendering. Note that WIC bitmap render targets do not support hardware rendering.

### -field pixelFormat

Type: <b><a href="/windows/win32/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

The pixel format and alpha mode of the render target. You can use the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-pixelformat">D2D1::PixelFormat</a> function to create a pixel format that specifies that Direct2D should select the pixel format and alpha mode for you. For a list of pixel formats and alpha modes supported by each render target, see <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

### -field dpiX

Type: <b>FLOAT</b>

The horizontal DPI of the render target.  To use the default DPI, set <i>dpiX</i> and <i>dpiY</i> to 0. For more information, see the Remarks section.

### -field dpiY

Type: <b>FLOAT</b>

The vertical DPI of the render target. To use the default DPI, set <i>dpiX</i> and <i>dpiY</i> to 0.  For more information, see the Remarks section.

### -field usage

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage">D2D1_RENDER_TARGET_USAGE</a></b>

A value that specifies how the render target is remoted and whether it should be GDI-compatible.  Set to <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage">D2D1_RENDER_TARGET_USAGE_NONE</a> to create a render target that is not compatible with GDI and uses Direct3D command-stream remoting if it  is available.

### -field minLevel

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_feature_level">D2D1_FEATURE_LEVEL</a></b>

A value that specifies the minimum Direct3D feature level required for hardware rendering. If the specified minimum level is not available, the render target uses software rendering if the <b>type </b> member is set to <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_type">D2D1_RENDER_TARGET_TYPE_DEFAULT</a>; if  <b>type </b> is set to <b>D2D1_RENDER_TARGET_TYPE_HARDWARE</b>, render target creation fails. A value of <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_feature_level">D2D1_FEATURE_LEVEL_DEFAULT</a> indicates that Direct2D should determine whether the Direct3D feature level of the device is adequate. This field is used only when creating <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> and <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a> objects.

## -remarks

Use this structure when creating a render target, or use it with the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties_)">ID2D1RenderTarget::IsSupported</a> method to check the properties supported by an existing render target.

As a convenience, Direct2D provides the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-rendertargetproperties">D2D1::RenderTargetProperties</a> helper function for creating <b>D2D1_RENDER_TARGET_PROPERTIES</b> structures. An easy way to create a <b>D2D1_RENDER_TARGET_PROPERTIES</b> structure that works for most render targets is to call the function without specifying any parameters. Doing so creates a <b>D2D1_RENDER_TARGET_PROPERTIES</b> structure that has its fields set to default values. For more information, see   <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-rendertargetproperties">D2D1::RenderTargetProperties</a>.

Not all render targets support hardware rendering. For a list, see the <a href="/windows/win32/Direct2D/render-targets-overview">Render Targets Overview</a>.

<h3><a id="Using_Default_DPI_Settings"></a><a id="using_default_dpi_settings"></a><a id="USING_DEFAULT_DPI_SETTINGS"></a>Using Default DPI Settings</h3>
To use the default DPI, set <i>dpiX</i> and <i>dpiY</i> to 0. The default DPI varies depending on the render target:

<ul>
<li>For a compatible render target, the default DPI is the DPI of the parent render target.</li>
<li>For a <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, the default DPI is the system DPI obtained from the render target's <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.</li>
<li>For other render targets, the default DPI is 96.</li>
</ul>
To use the default DPI setting, both <i>dpiX</i> and <i>dpiY</i> must be set to 0. Setting only one value to 0 causes an  <a href="/windows/win32/Direct2D/direct2d-error-codes">E_INVALIDARG</a> error when attempting to create a render target.


## Examples

The following example uses the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-rendertargetproperties">D2D1::RenderTargetProperties</a> function to create a <b>D2D1_RENDER_TARGET_PROPERTIES</b> structure suitable for most render targets. 


```cpp
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );

```

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties_)">ID2D1RenderTarget::IsSupported</a>



<a href="/windows/win32/Direct2D/render-targets-overview">Render Targets Overview</a>

