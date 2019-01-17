---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateGradientStopCollection
title: ID2D1DeviceContext::CreateGradientStopCollection
author: windows-sdk-content
description: Creates a gradient stop collection, enabling the gradient to contain color channels with values outside of [0,1] and also enabling rendering to a high-color render target with interpolation in sRGB space.
old-location: direct2d\id2d1devicecontext_creategradientstopcollection.htm
tech.root: Direct2D
ms.assetid: 6374fc62-1f54-4112-8ba3-9c1167bf8685
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection method [Direct2D], CreateGradientStopCollection method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateGradientStopCollection method, ID2D1DeviceContext.CreateGradientStopCollection, ID2D1DeviceContext::CreateGradientStopCollection, d2d1_1/ID2D1DeviceContext::CreateGradientStopCollection, direct2d.id2d1devicecontext_creategradientstopcollection
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.CreateGradientStopCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateGradientStopCollection


## -description


Creates a gradient stop collection, enabling the gradient to contain color channels with values outside of [0,1] and also enabling rendering to a high-color render target with interpolation in sRGB space.


## -parameters




### -param straightAlphaGradientStops

Type: <b>const <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>*</b>

An array of color values and offsets.


### -param straightAlphaGradientStopsCount

Type: <b>UINT</b>

The number of elements in the <i>gradientStops</i> array.


### -param preInterpolationSpace

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

Specifies both the input color space and the space in which the color interpolation occurs.


### -param postInterpolationSpace

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

The color space that colors will be converted to after interpolation occurs.


### -param bufferPrecision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The precision of the texture used to hold interpolated values.

<div class="alert"><b>Note</b>  This method will fail if the underlying Direct3D device does not support the requested buffer precision.  Use <a href="https://msdn.microsoft.com/c65824dc-a9d5-4d4d-a2de-b4283153f64f">ID2D1DeviceContext::IsBufferPrecisionSupported</a> to determine what is supported.
</div>
<div> </div>

### -param extendMode

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

Defines how colors outside of the range defined by the stop collection are determined.


### -param colorInterpolationMode

Type: <b><a href="https://msdn.microsoft.com/E3E9FB4C-5E77-451B-ABED-39D9C7AE567A">D2D1_COLOR_INTERPOLATION_MODE</a></b>

Defines how colors are interpolated.  D2D1_COLOR_INTERPOLATION_MODE_PREMULTIPLIED is the default, see Remarks for more info.


### -param gradientStopCollection1 [out]

Type: <b><a href="https://msdn.microsoft.com/aa423e18-c6b5-4587-b044-deda00a84615">ID2D1GradientStopCollection1</a>**</b>

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


You must always specify colors in straight alpha, regardless of interpolation mode being premultiplied or straight. The interpolation mode only affects the interpolated values. Likewise, the stops returned by <a href="https://msdn.microsoft.com/a5ae1b14-2694-4593-8eba-17d93b45bb9c">ID2D1GradientStopCollection::GetGradientStops</a> will always have straight alpha. 

If you specify <a href="https://msdn.microsoft.com/E3E9FB4C-5E77-451B-ABED-39D9C7AE567A">D2D1_COLOR_INTERPOLATION_MODE_PREMULTIPLIED</a>, then all stops are premultiplied before interpolation, and then un-premultiplied before color conversion.


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




<a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a>



<a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a>



<a href="https://msdn.microsoft.com/52c7fe56-9184-4095-86b1-6af23ef449f1">D2D1_GAMMA_CONVERSION</a>



<a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/aa423e18-c6b5-4587-b044-deda00a84615">ID2D1GradientStopCollection1</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742781(v=VS.85).aspx">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

