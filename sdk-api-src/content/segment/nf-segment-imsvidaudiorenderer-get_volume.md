---
UID: NF:segment.IMSVidAudioRenderer.get_Volume
title: IMSVidAudioRenderer::get_Volume
author: windows-driver-content
description: The get_Volume method retrieves the audio renderer's volume level.
old-location: mstv\imsvidaudiorenderer_get_volume.htm
old-project: mstv
ms.assetid: 7dbbdb17-b077-4e36-a5d4-c8e343feb930
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidAudioRenderer interface [Microsoft TV Technologies],get_Volume method, IMSVidAudioRenderer.get_Volume, IMSVidAudioRenderer::get_Volume, IMSVidAudioRendererget_Volume, get_Volume, get_Volume method [Microsoft TV Technologies], get_Volume method [Microsoft TV Technologies],IMSVidAudioRenderer interface, mstv.imsvidaudiorenderer_get_volume, segment/IMSVidAudioRenderer::get_Volume
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
-	IMSVidAudioRenderer.get_Volume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidAudioRenderer::get_Volume


## -description


The <b>get_Volume</b> method retrieves the audio renderer's volume level.


## -parameters




### -param lVol






#### - plVol [out]


            Pointer to a variable that receives the volume level, in units of .01 decibel (dB).
          


## -returns




            If the method succeeds, it returns S_OK. If it fails, it returns an error code.
          




## -remarks



Full volume is 0 and silence is –10,000. Divide by 100 to get the equivalent decibel value; for example, –10,000 is –100 dB.




## -see-also




<a href="https://msdn.microsoft.com/3258da5a-ab44-4c8a-813b-79a0c28693a3">IBasicAudio::get_Volume</a>



<a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer Interface</a>



<a href="https://msdn.microsoft.com/a0fa96bb-a903-41e1-bd2a-6ef1733adbd4">IMSVidAudioRenderer::put_Volume</a>
 

 

