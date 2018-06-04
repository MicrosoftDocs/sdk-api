---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

