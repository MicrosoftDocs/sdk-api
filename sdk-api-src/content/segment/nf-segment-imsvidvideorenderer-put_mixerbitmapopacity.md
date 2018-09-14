---
UID: NF:segment.IMSVidVideoRenderer.put_MixerBitmapOpacity
title: IMSVidVideoRenderer::put_MixerBitmapOpacity
author: windows-sdk-content
description: The put_MixerBitmapOpacity method specifies the opacity of the static bitmap image.
old-location: mstv\imsvidvideorenderer_put_mixerbitmapopacity.htm
tech.root: MSTV
ms.assetid: 5dba67ab-9522-48a3-be09-8ed8c27bffee
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_MixerBitmapOpacity method, IMSVidVideoRenderer.put_MixerBitmapOpacity, IMSVidVideoRenderer::put_MixerBitmapOpacity, IMSVidVideoRendererput_MixerBitmapOpacity, mstv.imsvidvideorenderer_put_mixerbitmapopacity, put_MixerBitmapOpacity, put_MixerBitmapOpacity method [Microsoft TV Technologies], put_MixerBitmapOpacity method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_MixerBitmapOpacity
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMSVidVideoRenderer.put_MixerBitmapOpacity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::put_MixerBitmapOpacity


## -description


The <b>put_MixerBitmapOpacity</b> method specifies the opacity of the static bitmap image.


## -parameters




### -param opacity [in]

Specifies the opacity as an integer from 0 (transparent) to 100 (opaque).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the static bitmap image is set, the VMR alpha blends the bitmap onto the video image, using the specified opacity.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/a91561e3-469b-412a-b5ab-af2a5a0855a6">IMSVidVideoRenderer::SetupMixerBitmap</a>



<a href="https://msdn.microsoft.com/830eff1a-e70e-440c-81be-69058d14f314">IMSVidVideoRenderer::get_MixerBitmapOpacity</a>



<a href="https://msdn.microsoft.com/fa9d9bea-f711-42f1-a247-322036744c44">IMSVidVideoRenderer::put_MixerBitmap</a>
 

 

