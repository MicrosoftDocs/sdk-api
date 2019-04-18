---
UID: NF:segment.IMSVidVideoRenderer.put__MixerBitmap
title: IMSVidVideoRenderer::put__MixerBitmap (segment.h)
author: windows-sdk-content
description: The put__MixerBitmap method specifies the static bitmap image.
old-location: mstv\imsvidvideorenderer_put__mixerbitmap.htm
tech.root: mstv
ms.assetid: 6dd7b83e-6ed6-4c57-8a00-a4ed2c78840d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__MixerBitmap method, IMSVidVideoRenderer.put__MixerBitmap, IMSVidVideoRenderer::put__MixerBitmap, IMSVidVideoRendererput__MixerBitmap, mstv.imsvidvideorenderer_put__mixerbitmap, put__MixerBitmap, put__MixerBitmap method [Microsoft TV Technologies], put__MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__MixerBitmap
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
 - IMSVidVideoRenderer.put__MixerBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer::put__MixerBitmap


## -description


The <b>put__MixerBitmap</b> method specifies the static bitmap image.


## -parameters




### -param MixerPicture [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd407381(v=VS.85).aspx">VMRALPHABITMAP</a> structure that contains information about the bitmap.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694747(v=VS.85).aspx">IMSVidVideoRenderer::get__MixerBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694751(v=VS.85).aspx">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

