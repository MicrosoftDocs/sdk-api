---
UID: NN:vmr9.IVMRMixerBitmap9
title: IVMRMixerBitmap9 (vmr9.h)
description: The IVMRMixerBitmap9 interface enables an application to blend a static image from a bitmap or Direct3D surface onto the video stream, when using the Video Mixing Renderer Filter 9 (VMR-9).You can pass images to the VMR as frequently as you like, but changing the image several times per second may impact the performance and smoothness of the video being rendered. The new image will be blended with the next and all subsequent video frames rendered by the VMR.Internally, the VMR uses its mixer component to perform the blending operation. In the VMR-9, the mixer is always present by default except in &#0034;renderless&#0034; mode in which the application is performing its own rendering. The image can contain embedded per pixel alpha information; this allows the image to contain regions that are transparent. Transparent areas can also be identified by a color key value. Changes in the image are only shown on the screen while the filter graph is running.
helpviewer_keywords: ["IVMRMixerBitmap9","IVMRMixerBitmap9 interface [DirectShow]","IVMRMixerBitmap9 interface [DirectShow]","described","IVMRMixerBitmap9Interface","dshow.ivmrmixerbitmap9","vmr9/IVMRMixerBitmap9"]
old-location: dshow\ivmrmixerbitmap9.htm
tech.root: dshow
ms.assetid: de48307a-3522-49a0-b0a5-73ce7cf90517
ms.date: 12/05/2018
ms.keywords: IVMRMixerBitmap9, IVMRMixerBitmap9 interface [DirectShow], IVMRMixerBitmap9 interface [DirectShow],described, IVMRMixerBitmap9Interface, dshow.ivmrmixerbitmap9, vmr9/IVMRMixerBitmap9
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRMixerBitmap9
 - vmr9/IVMRMixerBitmap9
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerBitmap9
---

# IVMRMixerBitmap9 interface


## -description

The <b>IVMRMixerBitmap9</b> interface enables an application to blend a static image from a bitmap or Direct3D surface onto the video stream, when using the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9).

You can pass images to the VMR as frequently as you like, but changing the image several times per second may impact the performance and smoothness of the video being rendered. The new image will be blended with the next and all subsequent video frames rendered by the VMR.

Internally, the VMR uses its mixer component to perform the blending operation. In the VMR-9, the mixer is always present by default except in "renderless" mode in which the application is performing its own rendering. The image can contain embedded per pixel alpha information; this allows the image to contain regions that are transparent. Transparent areas can also be identified by a color key value. Changes in the image are only shown on the screen while the filter graph is running.

## -inheritance

The <b>IVMRMixerBitmap9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRMixerBitmap9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/displaying-an-application-supplied-bitmap-on-the-composited-image">Displaying an Application-Supplied Bitmap on the Composited Image</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>
