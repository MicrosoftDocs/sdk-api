---
UID: NF:segment.IMSVidVideoRenderer.get__MixerBitmap
title: IMSVidVideoRenderer::get__MixerBitmap
author: windows-sdk-content
description: The get__MixerBitmap method retrieves the Video Mixing Renderer's IVMRMixerBitmap interface, which controls how the VMR mixes a static bitmap.
old-location: mstv\imsvidvideorenderer_get__mixerbitmap.htm
tech.root: mstv
ms.assetid: 714b8222-ab8b-4ece-8ae5-61bb41a7ed3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__MixerBitmap method, IMSVidVideoRenderer.get__MixerBitmap, IMSVidVideoRenderer::get__MixerBitmap, IMSVidVideoRendererget__MixerBitmap, get__MixerBitmap, get__MixerBitmap method [Microsoft TV Technologies], get__MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__mixerbitmap, segment/IMSVidVideoRenderer::get__MixerBitmap
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get__MixerBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::get__MixerBitmap


## -description


The <b>get__MixerBitmap</b> method retrieves the Video Mixing Renderer's <a href="https://msdn.microsoft.com/en-us/library/Dd390448(v=VS.85).aspx">IVMRMixerBitmap</a> interface, which controls how the VMR mixes a static bitmap.


## -parameters




### -param MixerPicture [out]

Receives an <a href="https://msdn.microsoft.com/en-us/library/Dd390448(v=VS.85).aspx">IVMRMixerBitmap</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The returned <a href="https://msdn.microsoft.com/en-us/library/Dd390448(v=VS.85).aspx">IVMRMixerBitmap</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694739(v=VS.85).aspx">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694759(v=VS.85).aspx">IMSVidVideoRenderer::put__MixerBitmap</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

