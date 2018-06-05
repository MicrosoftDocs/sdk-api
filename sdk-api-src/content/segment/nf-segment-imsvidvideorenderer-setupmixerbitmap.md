---
UID: NF:segment.IMSVidVideoRenderer.SetupMixerBitmap
title: IMSVidVideoRenderer::SetupMixerBitmap
author: windows-sdk-content
description: The SetupMixerBitmap method configures the Video Mixing Renderer (VMR) to display an alpha-blended bitmap on top of the video.
old-location: mstv\imsvidvideorenderer_setupmixerbitmap.htm
old-project: mstv
ms.assetid: a91561e3-469b-412a-b5ab-af2a5a0855a6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],SetupMixerBitmap method, IMSVidVideoRenderer.SetupMixerBitmap, IMSVidVideoRenderer::SetupMixerBitmap, IMSVidVideoRendererSetupMixerBitmap, SetupMixerBitmap, SetupMixerBitmap method [Microsoft TV Technologies], SetupMixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_setupmixerbitmap, segment/IMSVidVideoRenderer::SetupMixerBitmap
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
-	IMSVidVideoRenderer.SetupMixerBitmap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::SetupMixerBitmap


## -description


The <b>SetupMixerBitmap</b> method configures the Video Mixing Renderer (VMR) to display an alpha-blended bitmap on top of the video.


## -parameters




### -param MixerPictureDisp




### -param Opacity [in]

Specifies the opacity of the bitmap, as an integer from 0 (transparent) to 100 (opaque).


### -param rDest






#### - pMixerPictureDisp [in]

Pointer to an <b>IPictureDisp</b> interface that specifies the bitmap.


#### - prDest [in]

Pointer to an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface that specifies the position of the bitmap, relative to the video window.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/fa9d9bea-f711-42f1-a247-322036744c44">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="https://msdn.microsoft.com/5dba67ab-9522-48a3-be09-8ed8c27bffee">IMSVidVideoRenderer::put_MixerBitmapOpacity</a>



<a href="https://msdn.microsoft.com/05542d75-1723-4581-ac8b-6a577e0085cb">IMSVidVideoRenderer::put_MixerBitmapPositionRect</a>
 

 

