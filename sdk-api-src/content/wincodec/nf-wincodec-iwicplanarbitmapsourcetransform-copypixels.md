---
UID: NF:wincodec.IWICPlanarBitmapSourceTransform.CopyPixels
title: IWICPlanarBitmapSourceTransform::CopyPixels (wincodec.h)
description: Copies pixels into the destination planes. Configured by the supplied input parameters.
helpviewer_keywords: ["CopyPixels","CopyPixels method [Windows Imaging Component]","CopyPixels method [Windows Imaging Component]","IWICPlanarBitmapSourceTransform interface","IWICPlanarBitmapSourceTransform interface [Windows Imaging Component]","CopyPixels method","IWICPlanarBitmapSourceTransform.CopyPixels","IWICPlanarBitmapSourceTransform::CopyPixels","wic.iwicplanarbitmapsourcetransform_copypixels","wincodec/IWICPlanarBitmapSourceTransform::CopyPixels"]
old-location: wic\iwicplanarbitmapsourcetransform_copypixels.htm
tech.root: wic
ms.assetid: 0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01
ms.date: 12/05/2018
ms.keywords: CopyPixels, CopyPixels method [Windows Imaging Component], CopyPixels method [Windows Imaging Component],IWICPlanarBitmapSourceTransform interface, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],CopyPixels method, IWICPlanarBitmapSourceTransform.CopyPixels, IWICPlanarBitmapSourceTransform::CopyPixels, wic.iwicplanarbitmapsourcetransform_copypixels, wincodec/IWICPlanarBitmapSourceTransform::CopyPixels
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPlanarBitmapSourceTransform::CopyPixels
 - wincodec/IWICPlanarBitmapSourceTransform::CopyPixels
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPlanarBitmapSourceTransform.CopyPixels
---

# IWICPlanarBitmapSourceTransform::CopyPixels


## -description

Copies pixels into the destination planes.  Configured by the supplied input parameters.  

If a <i>dstTransform</i>, scale, or format conversion is specified, <i>cbStride</i> is the transformed stride and is based on the destination pixel format of the <i>pDstPlanes</i> parameter, not the original source's pixel format.

## -parameters

### -param prcSource [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The source rectangle of pixels to copy.

### -param uiWidth

Type: <b>UINT</b>

The width to scale the source bitmap.  This parameter must be equal to a value obtainable through <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform:: DoesSupportTransform</a>.

### -param uiHeight

Type: <b>UINT</b>

The height to scale the source bitmap.  This parameter must be equal to a value obtainable through <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform:: DoesSupportTransform</a>.

### -param dstTransform

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a></b>

The desired rotation or flip to perform prior to the pixel copy.  A rotate can be combined with a flip horizontal or a flip vertical, see <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a>.

### -param dstPlanarOptions [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptions</a></b>

Used to specify additional configuration options for the transform.  See <a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptions</a> for more detail.

WIC JPEG Decoder:
<a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptionsPreserveSubsampling</a> can be specified to retain the subsampling ratios when downscaling.  By default, the JPEG decoder attempts to preserve quality by downscaling only the Y plane in some cases, changing the image to 4:4:4 chroma subsampling.

### -param pDstPlanes

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicbitmapplane">WICBitmapPlane</a></b>

Specifies the pixel format and output buffer for each component plane.  The number of planes and pixel format of each plane must match values obtainable through  <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>.

### -param cPlanes

Type: <b>UINT</b>

The number of component planes specified by the <i>pDstPlanes</i> parameter.

## -returns

Type: <b>HRESULT</b>

If the specified scale, flip/rotate, and planar format configuration is not supported this method fails with <b>WINCODEC_ERR_INVALIDPARAMETER</b>.  You can check if a transform is supported by calling <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>.

## -remarks

WIC JPEG Decoder:
Depending on the configured chroma subsampling of the image, the source rectangle has the following restrictions:


<table>
<tr>
<th>Chroma Subsampling</th>
<th>X Coordinate</th>
<th>Y Coordinate</th>
<th>Chroma Width</th>
<th>Chroma Height</th>
</tr>
<tr>
<td>4:2:0</td>
<td>Multiple of 2</td>
<td>Multiple of 2</td>
<td>lumaWidth / 2 Rounded up to the nearest integer.</td>
<td>lumaHeight / 2 Rounded up to the nearest integer.</td>
</tr>
<tr>
<td>4:2:2</td>
<td>Multiple of 2</td>
<td>Any</td>
<td>lumaWidth / 2 Rounded up to the nearest integer.</td>
<td>lumaHeight</td>
</tr>
<tr>
<td>4:4:4</td>
<td>Any</td>
<td>Any</td>
<td>llumaWidth</td>
<td>llumaHeight</td>
</tr>
<tr>
<td>4:4:0</td>
<td>Any</td>
<td>Multiple of 2</td>
<td>lumaWidth</td>
<td>llumaHeight / 2 Rounded up to the nearest integer.</td>
</tr>
</table>
 

The <i>pDstPlanes</i> parameter supports the following pixel formats.

<table>
<tr>
<th>Plane Count</th>
<th>Plane 1</th>
<th>Plane 2</th>
<th>Plane 3</th>
</tr>
<tr>
<td>3</td>
<td>GUID_WICPixelFormat8bppY</td>
<td>GUID_WICPixelFormat8bppCb</td>
<td>GUID_WICPixelFormat8bppCr</td>
</tr>
<tr>
<td>2</td>
<td>GUID_WICPixelFormat8bppY</td>
<td>GUID_WICPixelFormat16bppCbCr</td>
<td>N/A</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform">IWICPlanarBitmapSourceTransform</a>