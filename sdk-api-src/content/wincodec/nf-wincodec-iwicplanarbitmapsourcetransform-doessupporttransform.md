---
UID: NF:wincodec.IWICPlanarBitmapSourceTransform.DoesSupportTransform
title: IWICPlanarBitmapSourceTransform::DoesSupportTransform (wincodec.h)
description: Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is.
helpviewer_keywords: ["DoesSupportTransform","DoesSupportTransform method [Windows Imaging Component]","DoesSupportTransform method [Windows Imaging Component]","IWICPlanarBitmapSourceTransform interface","IWICPlanarBitmapSourceTransform interface [Windows Imaging Component]","DoesSupportTransform method","IWICPlanarBitmapSourceTransform.DoesSupportTransform","IWICPlanarBitmapSourceTransform::DoesSupportTransform","wic.iwicplanarbitmapsourcetransform_doessupporttransform","wincodec/IWICPlanarBitmapSourceTransform::DoesSupportTransform"]
old-location: wic\iwicplanarbitmapsourcetransform_doessupporttransform.htm
tech.root: wic
ms.assetid: CB601454-591B-4292-A8BF-EA9D1F060AB3
ms.date: 12/05/2018
ms.keywords: DoesSupportTransform, DoesSupportTransform method [Windows Imaging Component], DoesSupportTransform method [Windows Imaging Component],IWICPlanarBitmapSourceTransform interface, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],DoesSupportTransform method, IWICPlanarBitmapSourceTransform.DoesSupportTransform, IWICPlanarBitmapSourceTransform::DoesSupportTransform, wic.iwicplanarbitmapsourcetransform_doessupporttransform, wincodec/IWICPlanarBitmapSourceTransform::DoesSupportTransform
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
 - IWICPlanarBitmapSourceTransform::DoesSupportTransform
 - wincodec/IWICPlanarBitmapSourceTransform::DoesSupportTransform
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
 - IWICPlanarBitmapSourceTransform.DoesSupportTransform
---

# IWICPlanarBitmapSourceTransform::DoesSupportTransform


## -description

Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is.   Otherwise, callers should fall back to <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> or <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> and retrieve interleaved pixels.

The following transforms can be checked:<ul>
<li>	Determine if the flip/rotate option specified via <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a> is supported.</li>
<li>Determine if the requested planar pixel format configuration is supported.</li>
<li>Determine the closest dimensions the implementation can natively scale to given the desired dimensions. 
</li>
</ul>


When a transform is supported, this method returns the description of the resulting planes in the <i>pPlaneDescriptions</i> parameter.

## -parameters

### -param puiWidth [in, out]

Type: <b>UINT*</b>

On input, the desired width.  On output, the closest supported width to the desired width; this is the same size or larger than the desired width.

### -param puiHeight [in, out]

Type: <b>UINT*</b>

On input, the desired height.  On output, the closest supported height to the desired height; this is the same size or larger than the desired width.

### -param dstTransform

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a></b>

The desired rotation or flip operation.  Multiple  <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a> can be combined in this flag parameter, see <b>WICBitmapTransformOptions</b>.

### -param dstPlanarOptions

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptions</a></b>

Used to specify additional configuration options for the transform.  See <a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptions</a> for more detail.



WIC JPEG Decoder:


<a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptionsPreserveSubsampling</a> can be specified to retain the subsampling ratios when downscaling.  By default, the JPEG decoder attempts to preserve quality by downscaling only the Y plane in some cases, changing the image to 4:4:4 chroma subsampling.

### -param pguidDstFormats [in]

Type: <b>const WICPixelFormatGUID*</b>

The requested pixel formats of the respective planes.

### -param pPlaneDescriptions [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicbitmapplanedescription">WICBitmapPlaneDescription</a>*</b>

When *<i>pfIsSupported</i> == TRUE, the array of plane descriptions contains the size and format of each of the planes.



WIC JPEG Decoder: The Cb and Cr planes can be a different size from the values returned by <i>puiWidth</i> and <i>puiHeight</i> due to chroma subsampling.

### -param cPlanes

Type: <b>UINT</b>

The number of component planes requested.

### -param pfIsSupported [out]

Type: <b>BOOL*</b>

Set to TRUE if the requested transforms are natively supported.

## -returns

Type: <b>HRESULT</b>

Check the value of <i>pfIsSupported</i> to determine if the transform is supported via <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels">IWICPlanarBitmapSourceTransform::CopyPixels</a>.  If this method fails, the output parameters for width, height, and plane descriptions are zero initialized.
Other return values indicate failure.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform">IWICPlanarBitmapSourceTransform</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels">IWicPlanarBitmapSourceTransform::CopyPixels</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicbitmapplanedescription">WICBitmapPlaneDescription</a>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicplanaroptions">WICPlanarOptions</a>