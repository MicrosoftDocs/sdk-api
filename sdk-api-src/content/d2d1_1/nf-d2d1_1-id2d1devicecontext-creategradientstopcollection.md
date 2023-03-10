---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateGradientStopCollection
title: ID2D1DeviceContext::CreateGradientStopCollection (d2d1_1.h)
description: Creates a gradient stop collection, enabling the gradient to contain color channels with values outside of [0,1] and also enabling rendering to a high-color render target with interpolation in sRGB space.
helpviewer_keywords: ["CreateGradientStopCollection","CreateGradientStopCollection method [Direct2D]","CreateGradientStopCollection method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateGradientStopCollection method","ID2D1DeviceContext.CreateGradientStopCollection","ID2D1DeviceContext::CreateGradientStopCollection","d2d1_1/ID2D1DeviceContext::CreateGradientStopCollection","direct2d.id2d1devicecontext_creategradientstopcollection"]
old-location: direct2d\id2d1devicecontext_creategradientstopcollection.htm
tech.root: Direct2D
ms.assetid: 6374fc62-1f54-4112-8ba3-9c1167bf8685
ms.date: 12/05/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection method [Direct2D], CreateGradientStopCollection method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateGradientStopCollection method, ID2D1DeviceContext.CreateGradientStopCollection, ID2D1DeviceContext::CreateGradientStopCollection, d2d1_1/ID2D1DeviceContext::CreateGradientStopCollection, direct2d.id2d1devicecontext_creategradientstopcollection
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1DeviceContext::CreateGradientStopCollection
 - d2d1_1/ID2D1DeviceContext::CreateGradientStopCollection
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
 - ID2D1DeviceContext.CreateGradientStopCollection
---

# ID2D1DeviceContext::CreateGradientStopCollection


## -description

Creates a gradient stop collection, enabling the gradient to contain color channels with values outside of [0,1] and also enabling rendering to a high-color render target with interpolation in sRGB space.

## -parameters

### -param straightAlphaGradientStops

Type: <b>const <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>*</b>

An array of color values and offsets.

### -param straightAlphaGradientStopsCount

Type: <b>UINT</b>

The number of elements in the <i>gradientStops</i> array.

### -param preInterpolationSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

Specifies both the input color space and the space in which the color interpolation occurs.

### -param postInterpolationSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

The color space that colors will be converted to after interpolation occurs.

### -param bufferPrecision

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

The precision of the texture used to hold interpolated values.

<div class="alert"><b>Note</b>  This method will fail if the underlying Direct3D device does not support the requested buffer precision.  Use <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported">ID2D1DeviceContext::IsBufferPrecisionSupported</a> to determine what is supported.
</div>
<div> </div>

### -param extendMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

Defines how colors outside of the range defined by the stop collection are determined.

### -param colorInterpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_interpolation_mode">D2D1_COLOR_INTERPOLATION_MODE</a></b>

Defines how colors are interpolated.  D2D1_COLOR_INTERPOLATION_MODE_PREMULTIPLIED is the default, see Remarks for more info.

### -param gradientStopCollection1 [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1">ID2D1GradientStopCollection1</a>**</b>

The new gradient stop collection.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>

## -remarks

This method linearly interpolates between the color stops. An optional color space conversion is applied post-interpolation. Whether and how this gamma conversion is applied is determined by the pre- and post-interpolation. This method will fail if the device context does not support the requested buffer precision.

In order to get the desired result, you need to ensure that the inputs are specified in the correct color space. 


You must always specify colors in straight alpha, regardless of interpolation mode being premultiplied or straight. The interpolation mode only affects the interpolated values. Likewise, the stops returned by <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1gradientstopcollection-getgradientstops">ID2D1GradientStopCollection::GetGradientStops</a> will always have straight alpha. 

If you specify <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_interpolation_mode">D2D1_COLOR_INTERPOLATION_MODE_PREMULTIPLIED</a>, then all stops are premultiplied before interpolation, and then un-premultiplied before color conversion.


Starting with Windows 8, the interpolation behavior of this method has changed.  

The table here shows the behavior in Windows 7 and earlier.

<table>
<tr>
<th>Gamma</th>
<th>Before Interpolation Behavior</th>
<th>After Interpolation Behavior</th>
<th>GetColorInteroplationGamma
(output color space)
</th>
</tr>
<tr>
<td>1.0</td>
<td>Clamps the inputs and then converts from sRGB to scRGB.</td>
<td>Converts from scRGB to sRGB post-interpolation.</td>
<td>1.0</td>
</tr>
<tr>
<td>2.2</td>
<td>Clamps the inputs.</td>
<td>No Operation</td>
<td>2.2</td>
</tr>
</table>
 

The table here shows the behavior in Windows 8 and later.

<table>
<tr>
<th>Gamma</th>
<th>Before Interpolation Behavior</th>
<th>After Interpolation Behavior</th>
<th>GetColorInteroplationGamma
(output color space)
</th>
</tr>
<tr>
<td>sRGB to scRGB</td>
<td>No Operation</td>
<td>Clamps the outputs and then converts from sRGB to scRGB.</td>
<td>1.0</td>
</tr>
<tr>
<td>scRGB to sRGB</td>
<td>No Operation</td>
<td>Clamps the outputs and then converts from sRGB to scRGB.</td>
<td>2.2</td>
</tr>
<tr>
<td>sRGB to sRGB</td>
<td>No Operation</td>
<td>No Operation</td>
<td>2.2</td>
</tr>
<tr>
<td>scRGB to scRGB</td>
<td>No Operation</td>
<td>No Operation</td>
<td>1.0</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a>



<a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a>



<a href="/previous-versions/windows/desktop/legacy/hh447002(v=vs.85)">D2D1_GAMMA_CONVERSION</a>



<a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1">ID2D1GradientStopCollection1</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>