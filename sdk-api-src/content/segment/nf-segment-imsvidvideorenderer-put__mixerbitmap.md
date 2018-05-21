---
UID: NF:segment.IMSVidVideoRenderer.put__MixerBitmap
title: IMSVidVideoRenderer::put__MixerBitmap
author: windows-driver-content
description: The put__MixerBitmap method specifies the static bitmap image.
old-location: mstv\imsvidvideorenderer_put__mixerbitmap.htm
old-project: mstv
ms.assetid: 6dd7b83e-6ed6-4c57-8a00-a4ed2c78840d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__MixerBitmap method, IMSVidVideoRenderer.put__MixerBitmap, IMSVidVideoRenderer::put__MixerBitmap, IMSVidVideoRendererput__MixerBitmap, mstv.imsvidvideorenderer_put__mixerbitmap, put__MixerBitmap, put__MixerBitmap method [Microsoft TV Technologies], put__MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__MixerBitmap
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.put__MixerBitmap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRenderer::put__MixerBitmap


## -description


The <b>put__MixerBitmap</b> method specifies the static bitmap image.


## -parameters




### -param MixerPicture






#### - pMixerPicture [in]

A pointer to a <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure that contains information about the bitmap.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/714b8222-ab8b-4ece-8ae5-61bb41a7ed3c">IMSVidVideoRenderer::get__MixerBitmap</a>



<a href="https://msdn.microsoft.com/fa9d9bea-f711-42f1-a247-322036744c44">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

