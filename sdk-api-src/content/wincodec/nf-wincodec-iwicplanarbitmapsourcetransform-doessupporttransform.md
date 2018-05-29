---
UID: NF:wincodec.IWICPlanarBitmapSourceTransform.DoesSupportTransform
title: IWICPlanarBitmapSourceTransform::DoesSupportTransform
author: windows-sdk-content
description: Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is.
old-location: wic\iwicplanarbitmapsourcetransform_doessupporttransform.htm
old-project: wic
ms.assetid: CB601454-591B-4292-A8BF-EA9D1F060AB3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: DoesSupportTransform, DoesSupportTransform method [Windows Imaging Component], DoesSupportTransform method [Windows Imaging Component],IWICPlanarBitmapSourceTransform interface, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],DoesSupportTransform method, IWICPlanarBitmapSourceTransform.DoesSupportTransform, IWICPlanarBitmapSourceTransform::DoesSupportTransform, wic.iwicplanarbitmapsourcetransform_doessupporttransform, wincodec/IWICPlanarBitmapSourceTransform::DoesSupportTransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICPlanarBitmapSourceTransform.DoesSupportTransform
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPlanarBitmapSourceTransform::DoesSupportTransform


## -description


Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is.   Otherwise, callers should fall back to <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a> or <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> and retrieve interleaved pixels.



The following transforms can be checked:<ul>
<li>	Determine if the flip/rotate option specified via <a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a> is supported.</li>
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

Type: <b><a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a></b>

The desired rotation or flip operation.  Multiple  <a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a> can be combined in this flag parameter, see <b>WICBitmapTransformOptions</b>.


### -param dstPlanarOptions

Type: <b><a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptions</a></b>

Used to specify additional configuration options for the transform.  See <a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptions</a> for more detail.



WIC JPEG Decoder:


<a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptionsPreserveSubsampling</a> can be specified to retain the subsampling ratios when downscaling.  By default, the JPEG decoder attempts to preserve quality by downscaling only the Y plane in some cases, changing the image to 4:4:4 chroma subsampling.



### -param pguidDstFormats [out]

Type: <b>const WICPixelFormatGUID*</b>

The requested pixel formats of the respective planes.

Type: <b><a href="https://msdn.microsoft.com/A5685E9B-F2B9-4A1B-9CEA-044E5FA1CC6D">WICBitmapPlaneDescription</a>*</b>

When *<i>pfIsSupported</i> == TRUE, the array of plane descriptions contains the size and format of each of the planes.



WIC JPEG Decoder: The Cb and Cr planes can be a different size from the values returned by <i>puiWidth</i> and <i>puiHeight</i> due to chroma subsampling.



### -param pPlaneDescriptions




### -param cPlanes

Type: <b>UINT</b>

The number of component planes requested.


### -param pfIsSupported [out]

Type: <b>BOOL*</b>

Set to TRUE if the requested transforms are natively supported.


## -returns



Type: <b>HRESULT</b>

Check the value of <i>pfIsSupported</i> to determine if the transform is supported via <a href="https://msdn.microsoft.com/0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01">IWICPlanarBitmapSourceTransform::CopyPixels</a>.  If this method fails, the output parameters for width, height, and plane descriptions are zero initialized.
Other return values indicate failure.






## -see-also




<a href="https://msdn.microsoft.com/AA47F10A-C90A-4DAF-973F-2669D7364CB9">IWICPlanarBitmapSourceTransform</a>



<a href="https://msdn.microsoft.com/0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01">IWicPlanarBitmapSourceTransform::CopyPixels</a>



<a href="https://msdn.microsoft.com/A5685E9B-F2B9-4A1B-9CEA-044E5FA1CC6D">WICBitmapPlaneDescription</a>



<a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a>



<a href="https://msdn.microsoft.com/8B7F34AA-77A0-428D-800E-31AB43067102">WICPlanarOptions</a>
 

 

