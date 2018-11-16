---
UID: NF:wincodec.IWICBitmapSourceTransform.CopyPixels
title: IWICBitmapSourceTransform::CopyPixels
author: windows-sdk-content
description: Copies pixel data using the supplied input parameters.
old-location: wic\_wic_codec_iwicbitmapsourcetransform_copypixels.htm
tech.root: wic
ms.assetid: c4c36750-bf30-4e58-aca6-bbb49c7cde4b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CopyPixels, CopyPixels method [Windows Imaging Component], CopyPixels method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],CopyPixels method, IWICBitmapSourceTransform.CopyPixels, IWICBitmapSourceTransform::CopyPixels, _wic_codec_iwicbitmapsourcetransform_copypixels, wic._wic_codec_iwicbitmapsourcetransform_copypixels, wincodec/IWICBitmapSourceTransform::CopyPixels
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICBitmapSourceTransform.CopyPixels
: 
---

# IWICBitmapSourceTransform::CopyPixels


## -description


Copies pixel data using the supplied input parameters.


## -parameters




### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/e07c26bf-b645-4382-bb93-8472ba397026">WICRect</a>*</b>

The rectangle of pixels to copy.


### -param uiWidth [in]

Type: <b>UINT</b>

The width to scale the source bitmap. This parameter must equal the value obtainable through <a href="https://msdn.microsoft.com/0eae79dc-d636-4449-ba90-0f296b71573a">IWICBitmapSourceTransform::GetClosestSize</a>.


### -param uiHeight [in]

Type: <b>UINT</b>

The height to scale the source bitmap. This parameter must equal the value obtainable through <a href="https://msdn.microsoft.com/0eae79dc-d636-4449-ba90-0f296b71573a">IWICBitmapSourceTransform::GetClosestSize</a>.


### -param pguidDstFormat [in]

Type: <b>WICPixelFormatGUID*</b>

The GUID of desired pixel format in which the pixels should be returned. 
               

This GUID must be a format obtained through an <a href="https://msdn.microsoft.com/153c5e2a-c42f-4949-9313-48d5e186ecf3">GetClosestPixelFormat</a> call.


### -param dstTransform [in]

Type: <b><a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a></b>

The desired rotation or flip to perform prior to the pixel copy.
               

The transform must be an operation supported by an <a href="https://msdn.microsoft.com/73f27e20-3245-42b3-8b83-29c3c969624f">DoesSupportTransform</a> call.

If a <i>dstTransform</i> is specified, <i>nStride</i> is the <i>transformed stride</i> and is based on the <i>pguidDstFormat</i> pixel format, not the original source's pixel format.


### -param nStride [in]

Type: <b>UINT</b>

The <a href="https://docs.microsoft.com/">stride</a> of the destination buffer.


### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the destination buffer.


### -param pbBuffer [out]

Type: <b>BYTE*</b>

The output buffer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<h3><a id="Codec_Developer_Remarks"></a><a id="codec_developer_remarks"></a><a id="CODEC_DEVELOPER_REMARKS"></a>Codec Developer Remarks</h3>
If NULL is passed in for <i>prc</i>, the entire image is copied.

For codec developer implementation details for this method, see <a href="https://msdn.microsoft.com/6a3e682c-55c6-4728-9d14-5eb0290f3dcc">Implementing IWICBitmapSourceTransform</a>.

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



<a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a>



<a href="https://msdn.microsoft.com/b872baf9-9fcb-4604-a518-26e109eda792">Microsoft Windows Imaging Codec</a>



<a href="https://msdn.microsoft.com/ed7987f0-5983-4bb5-8640-0830a87c8f2e">Programming Guide</a>



<a href="https://msdn.microsoft.com/5ffa52e9-c01e-455e-85dc-2b7c078cc252">References</a>



<a href="https://msdn.microsoft.com/0714f720-f06f-4480-bc3c-5cd0337510d7">Samples and Code Examples</a>
 

 

