---
UID: NF:d2d1.ID2D1RenderTarget.CreateCompatibleRenderTarget(constD2D1_SIZE_F,constD2D1_SIZE_U,constD2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget)
title: ID2D1RenderTarget::CreateCompatibleRenderTarget (d2d1.h)
description: Creates a new bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target .
helpviewer_keywords: ["CreateCompatibleRenderTarget","CreateCompatibleRenderTarget methods [Direct2D]","ID2D1RenderTarget.CreateCompatibleRenderTarget","ID2D1RenderTarget::CreateCompatibleRenderTarget","d2d1/CreateCompatibleRenderTarget","direct2d.id2d1rendertarget_createcompatiblerendertarget"]
old-location: direct2d\id2d1rendertarget_createcompatiblerendertarget.htm
tech.root: Direct2D
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
ms.date: 12/05/2018
ms.keywords: CreateCompatibleRenderTarget, CreateCompatibleRenderTarget methods [Direct2D], ID2D1RenderTarget.CreateCompatibleRenderTarget, ID2D1RenderTarget::CreateCompatibleRenderTarget, d2d1/CreateCompatibleRenderTarget, direct2d.id2d1rendertarget_createcompatiblerendertarget
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID2D1RenderTarget::CreateCompatibleRenderTarget
 - d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget
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
 - ID2D1RenderTarget::CreateCompatibleRenderTarget
---

## -description

Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target.

## -parameters

### -param desiredSize

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-size-f">D2D1_SIZE_F</a>*</b>

The desired size of the new render target (in device-independent pixels), if it should be different from the original render target. For more info, see the Remarks section.

### -param desiredPixelSize

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-size-u">D2D1_SIZE_U</a>*</b>

The desired size of the new render target in pixels if it should be different from the original render target. For more information, see the Remarks section.

### -param desiredFormat

Type: [in] <b>const <a href="/windows/win32/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a>*</b>

The desired pixel format and alpha mode of the new render target. If the pixel format is set to DXGI_FORMAT_UNKNOWN, the new render target uses the same pixel format as the original render target. If the alpha mode is <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_UNKNOWN</a>, the alpha mode of the new render target defaults to <b>D2D1_ALPHA_MODE_PREMULTIPLIED</b>. For information about supported pixel formats, see  <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>.

### -param options

Type: [in] <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_compatible_render_target_options">D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS</a></b>

A value that specifies whether the new render target must be compatible with GDI.

### -param bitmapRenderTarget

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a>**</b>

When this method returns, contains a pointer to a pointer to a new bitmap render target. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The pixel size and DPI of the new render target can be altered by specifying values for <i>desiredSize</i> or <i>desiredPixelSize</i>:  

<ul>
<li>If <i>desiredSize</i> is specified but <i>desiredPixelSize</i> is not, the pixel size is computed from the desired size using the parent target DPI. If the <i>desiredSize</i> maps to a integer-pixel size, the DPI of the compatible render target is the same as the DPI of the parent target.  If <i>desiredSize</i> maps to a fractional-pixel size, the pixel size is rounded up to the nearest integer and the DPI for the compatible render target is slightly higher than the DPI of the parent render target. In all cases, the coordinate (<i>desiredSize</i>.width, <i>desiredSize</i>.height) maps to the lower-right corner of the compatible render target.</li>
<li>If the <i>desiredPixelSize</i> is specified and <i>desiredSize</i>  is not, the DPI of the new render target is the same as the original render target.</li>
<li>If both <i>desiredSize</i>  and <i>desiredPixelSize</i> are specified, the DPI of the new render target is computed to account for the difference in scale.</li>
<li>If neither <i>desiredSize</i> nor <i>desiredPixelSize</i> is specified, the new render target size and DPI match the original render target. </li>
</ul>

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

