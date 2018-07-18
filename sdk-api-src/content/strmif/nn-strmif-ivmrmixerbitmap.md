---
UID: NN:strmif.IVMRMixerBitmap
title: IVMRMixerBitmap
author: windows-sdk-content
description: The IVMRMixerBitmap interface enables an application to blend a static image from a bitmap or DirectDraw surface onto the video stream, when using the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrmixerbitmap.htm
old-project: DirectShow
ms.assetid: ac7da3f9-2c17-4517-bb64-6b56257a65c3
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IVMRMixerBitmap, IVMRMixerBitmap interface [DirectShow], IVMRMixerBitmap interface [DirectShow],described, IVMRMixerBitmapInterface, dshow.ivmrmixerbitmap, strmif/IVMRMixerBitmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerBitmap
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerBitmap interface


## -description


The <b>IVMRMixerBitmap</b> interface enables an application to blend a static image from a bitmap or DirectDraw surface onto the video stream, when using the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7).


<div class="alert"><b>Note</b>  For the VMR-9, use the <a href="https://msdn.microsoft.com/de48307a-3522-49a0-b0a5-73ce7cf90517">IVMRMixerBitmap9</a> interface.</div>
<div> </div>


You can pass images to the VMR as frequently as you like, but changing the image several times per second may impact the performance and smoothness of the video being rendered. The new image will be blended with the next and all subsequent video frames rendered by the VMR.

Internally, the VMR uses its mixer component to perform the blending operation. Therefore the VMR must be configured correctly prior to commencing video playback. Even if only a single video stream is present, applications should call <a href="https://msdn.microsoft.com/cd200b33-bb74-474a-9047-d81cb470af23">IVMRFilterConfig::SetNumberOfStreams</a> with a value of "1" to cause the VMR to load the mixer and compositor. The image can contain embedded per pixel alpha information; this allows the image to contain regions that are transparent. Transparent areas can also be identified by a color key value. Changes in the image are only shown on the screen while the filter graph is running.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMixerBitmap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRMixerBitmap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRMixerBitmap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d03cc6ad-e09b-4af7-93b7-51880465c0b6">GetAlphaBitmapParameters</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the current image and related blending parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92e57c3a-6761-4a54-83f5-0ea0ce80d60b">SetAlphaBitmap</a>
</td>
<td align="left" width="63%">
Specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/039cb675-c384-4909-b06d-b331cc281df6">UpdateAlphaBitmapParameters</a>
</td>
<td align="left" width="63%">
Changes the bitmap location, size and blending value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c51329d3-e814-4ef9-aad8-a3e60f9fa2a7">Displaying an Application-Supplied Bitmap on the Composited Image</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a>
 

 

