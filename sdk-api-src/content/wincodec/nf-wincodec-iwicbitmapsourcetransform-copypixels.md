---
UID: NF:wincodec.IWICBitmapSourceTransform.CopyPixels
title: IWICBitmapSourceTransform::CopyPixels (wincodec.h)
description: Copies pixel data using the supplied input parameters.
helpviewer_keywords: ["CopyPixels","CopyPixels method [Windows Imaging Component]","CopyPixels method [Windows Imaging Component]","IWICBitmapSourceTransform interface","IWICBitmapSourceTransform interface [Windows Imaging Component]","CopyPixels method","IWICBitmapSourceTransform.CopyPixels","IWICBitmapSourceTransform::CopyPixels","_wic_codec_iwicbitmapsourcetransform_copypixels","wic._wic_codec_iwicbitmapsourcetransform_copypixels","wincodec/IWICBitmapSourceTransform::CopyPixels"]
old-location: wic\_wic_codec_iwicbitmapsourcetransform_copypixels.htm
tech.root: wic
ms.assetid: c4c36750-bf30-4e58-aca6-bbb49c7cde4b
ms.date: 12/05/2018
ms.keywords: CopyPixels, CopyPixels method [Windows Imaging Component], CopyPixels method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],CopyPixels method, IWICBitmapSourceTransform.CopyPixels, IWICBitmapSourceTransform::CopyPixels, _wic_codec_iwicbitmapsourcetransform_copypixels, wic._wic_codec_iwicbitmapsourcetransform_copypixels, wincodec/IWICBitmapSourceTransform::CopyPixels
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapSourceTransform::CopyPixels
 - wincodec/IWICBitmapSourceTransform::CopyPixels
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapSourceTransform.CopyPixels
---

# IWICBitmapSourceTransform::CopyPixels


## -description

Copies pixel data using the supplied input parameters.

## -parameters

### -param prc [in]

Type: <b>const <a href="/windows/win32/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The rectangle of pixels to copy.

### -param uiWidth [in]

Type: <b>UINT</b>

The width to scale the source bitmap. This parameter must equal the value obtainable through <a href="/windows/win32/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize">IWICBitmapSourceTransform::GetClosestSize</a>.

### -param uiHeight [in]

Type: <b>UINT</b>

The height to scale the source bitmap. This parameter must equal the value obtainable through <a href="/windows/win32/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize">IWICBitmapSourceTransform::GetClosestSize</a>.

### -param pguidDstFormat [in]

Type: <b>WICPixelFormatGUID*</b>

The GUID of desired pixel format in which the pixels should be returned. 
               

This GUID must be a format obtained through an <a href="/windows/win32/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat">GetClosestPixelFormat</a> call.

### -param dstTransform [in]

Type: <b><a href="/windows/win32/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a></b>

The desired rotation or flip to perform prior to the pixel copy.
               

The transform must be an operation supported by an <a href="/windows/win32/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform">DoesSupportTransform</a> call.

If a <i>dstTransform</i> is specified, <i>nStride</i> is the <i>transformed stride</i> and is based on the <i>pguidDstFormat</i> pixel format, not the original source's pixel format.

### -param nStride [in]

Type: <b>UINT</b>

The stride of the destination buffer.

### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the destination buffer.

### -param pbBuffer [out]

Type: <b>BYTE*</b>

The output buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<h3><a id="Codec_Developer_Remarks"></a><a id="codec_developer_remarks"></a><a id="CODEC_DEVELOPER_REMARKS"></a>Codec Developer Remarks</h3>
If NULL is passed in for <i>prc</i>, the entire image is copied.

For codec developer implementation details for this method, see <a href="/windows/win32/wic/-wic-imp-iwicbitmapsourcetransform">Implementing IWICBitmapSourceTransform</a>.

When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.
               To ensure predictability and consistency across CODECs, it's important that all CODECs perform these operations in the same order.
               The recommended order of these operations is:
               <ol>
<li>Scale</li>
<li>Crop</li>
<li>Flip/Rotate</li>
</ol>


Pixel format conversion can be performed at any time, since it has no effect on the other transforms.
            

The first parameter, <i>prc</i> is used to specify the region of interest for clipping the image.
               By convention, scaling is performed before clipping so, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.
            

If a <i>dstTransform</i> is specified, the stride is the transformed stride, and is based on the pixelFormat specified in the <b>CopyPixels</b> call, not the original frame's pixel format.

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a>



<a href="/windows/win32/wic/-wic-lh">Microsoft Windows Imaging Codec</a>



<a href="/windows/win32/wic/-wic-programming-guide">Programming Guide</a>



<a href="/windows/win32/wic/-wic-codec-reference">References</a>



<a href="/windows/win32/wic/-wic-samples">Samples and Code Examples</a>