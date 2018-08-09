---
UID: NF:wincodec.IWICPlanarBitmapSourceTransform.CopyPixels
title: IWICPlanarBitmapSourceTransform::CopyPixels
author: windows-sdk-content
description: Copies pixels into the destination planes. Configured by the supplied input parameters.
old-location: wic\iwicplanarbitmapsourcetransform_copypixels.htm
old-project: wic
ms.assetid: 0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CopyPixels, CopyPixels method [Windows Imaging Component], CopyPixels method [Windows Imaging Component],IWICPlanarBitmapSourceTransform interface, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],CopyPixels method, IWICPlanarBitmapSourceTransform.CopyPixels, IWICPlanarBitmapSourceTransform::CopyPixels, wic.iwicplanarbitmapsourcetransform_copypixels, wincodec/IWICPlanarBitmapSourceTransform::CopyPixels
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPlanarBitmapSourceTransform.CopyPixels
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPlanarBitmapSourceTransform::CopyPixels


## -description


Copies pixels into the destination planes.  Configured by the supplied input parameters.  

If a <i>dstTransform</i>, scale, or format conversion is specified, <i>cbStride</i> is the transformed stride and is based on the destination pixel format of the <i>pDstPlanes</i> parameter, not the original source's pixel format.


## -parameters




### -param prcSource [in]

Type: <b>const <a href="https://msdn.microsoft.com/e07c26bf-b645-4382-bb93-8472ba397026">WICRect</a>*</b>

The source rectangle of pixels to copy.  


### -param uiWidth

Type: <b>UINT</b>

The width to scale the source bitmap.  This parameter must be equal to a value obtainable through <a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">IWICPlanarBitmapSourceTransform:: DoesSupportTransform</a>.


### -param uiHeight

Type: <b>UINT</b>

The height to scale the source bitmap.  This parameter must be equal to a value obtainable through <a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">IWICPlanarBitmapSourceTransform:: DoesSupportTransform</a>.


### -param dstTransform

Type: <b><a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a></b>

The desired rotation or flip to perform prior to the pixel copy.  A rotate can be combined with a flip horizontal or a flip vertical, see <a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a>.


### -param dstPlanarOptions [in]

Type: <b>const <a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptions</a></b>

Used to specify additional configuration options for the transform.  See <a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptions</a> for more detail.

WIC JPEG Decoder:
<a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptionsPreserveSubsampling</a> can be specified to retain the subsampling ratios when downscaling.  By default, the JPEG decoder attempts to preserve quality by downscaling only the Y plane in some cases, changing the image to 4:4:4 chroma subsampling.



### -param pDstPlanes

Type: <b><a href="https://msdn.microsoft.com/4E988284-DE71-48B2-BF77-D616FAA2A3B1">WICBitmapPlane</a></b>

Specifies the pixel format and output buffer for each component plane.  The number of planes and pixel format of each plane must match values obtainable through  <a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>.


### -param cPlanes

Type: <b>UINT</b>

The number of component planes specified by the <i>pDstPlanes</i> parameter.


## -returns



Type: <b>HRESULT</b>

If the specified scale, flip/rotate, and planar format configuration is not supported this method fails with <b>WINCODEC_ERR_INVALIDPARAMETER</b>.  You can check if a transform is supported by calling <a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>.




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




<a href="https://msdn.microsoft.com/AA47F10A-C90A-4DAF-973F-2669D7364CB9">IWICPlanarBitmapSourceTransform</a>
 

 

