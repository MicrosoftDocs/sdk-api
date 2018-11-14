---
UID: NF:segment.IMSVidVideoRenderer.put_MixerBitmap
title: IMSVidVideoRenderer::put_MixerBitmap
author: windows-sdk-content
description: The put_MixerBitmap method specifies the static bitmap image, as an IPictureDisp type.
old-location: mstv\imsvidvideorenderer_put_mixerbitmap.htm
tech.root: MSTV
ms.assetid: fa9d9bea-f711-42f1-a247-322036744c44
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_MixerBitmap method, IMSVidVideoRenderer.put_MixerBitmap, IMSVidVideoRenderer::put_MixerBitmap, IMSVidVideoRendererput_MixerBitmap, mstv.imsvidvideorenderer_put_mixerbitmap, put_MixerBitmap, put_MixerBitmap method [Microsoft TV Technologies], put_MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_MixerBitmap
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
 - IMSVidVideoRenderer.put_MixerBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidVideoRenderer.put_MixerBitmap
: 
---

# IMSVidVideoRenderer::put_MixerBitmap


## -description


The <b>put_MixerBitmap</b> method specifies the static bitmap image, as an <b>IPictureDisp</b> type.


## -parameters




### -param MixerPictureDisp

TBD




#### - pMixerPictureDisp [in]

Specifies a pointer to the <b>IPictureDisp</b> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The VMR alpha-blends the static bitmap image onto the video image. For information about the <b>IPictureDisp</b> interface, see the Platform SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/a91561e3-469b-412a-b5ab-af2a5a0855a6">IMSVidVideoRenderer::SetupMixerBitmap</a>



<a href="https://msdn.microsoft.com/cfcfab14-7084-4716-8955-574168cd3506">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="https://msdn.microsoft.com/5dba67ab-9522-48a3-be09-8ed8c27bffee">IMSVidVideoRenderer::put_MixerBitmapOpacity</a>



<a href="https://msdn.microsoft.com/05542d75-1723-4581-ac8b-6a577e0085cb">IMSVidVideoRenderer::put_MixerBitmapPositionRect</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

