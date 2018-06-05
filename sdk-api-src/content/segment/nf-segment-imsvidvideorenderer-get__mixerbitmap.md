---
UID: NF:segment.IMSVidVideoRenderer.get__MixerBitmap
title: IMSVidVideoRenderer::get__MixerBitmap
author: windows-sdk-content
description: The get__MixerBitmap method retrieves the Video Mixing Renderer's IVMRMixerBitmap interface, which controls how the VMR mixes a static bitmap.
old-location: mstv\imsvidvideorenderer_get__mixerbitmap.htm
old-project: mstv
ms.assetid: 714b8222-ab8b-4ece-8ae5-61bb41a7ed3c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__MixerBitmap method, IMSVidVideoRenderer.get__MixerBitmap, IMSVidVideoRenderer::get__MixerBitmap, IMSVidVideoRendererget__MixerBitmap, get__MixerBitmap, get__MixerBitmap method [Microsoft TV Technologies], get__MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__mixerbitmap, segment/IMSVidVideoRenderer::get__MixerBitmap
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.get__MixerBitmap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get__MixerBitmap


## -description


The <b>get__MixerBitmap</b> method retrieves the Video Mixing Renderer's <a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap</a> interface, which controls how the VMR mixes a static bitmap.


## -parameters




### -param MixerPicture






#### - ppMixerPicture [out]

Receives an <a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The returned <a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/cfcfab14-7084-4716-8955-574168cd3506">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="https://msdn.microsoft.com/6dd7b83e-6ed6-4c57-8a00-a4ed2c78840d">IMSVidVideoRenderer::put__MixerBitmap</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

