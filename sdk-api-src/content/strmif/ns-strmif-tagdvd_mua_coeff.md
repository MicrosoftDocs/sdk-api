---
UID: NS:strmif.tagDVD_MUA_Coeff
title: tagDVD_MUA_Coeff
author: windows-sdk-content
description: The DVD_MUA_Coeff structure defines the mixing coefficients for one channel in a multichannel audio stream. The DVD_MultichannelAudioAttributes structure contains an array of eight DVD_MUA_Coeff structures, one for each channel in the stream.
old-location: dshow\dvd_mua_coeff.htm
tech.root: DirectShow
ms.assetid: 8b8402da-37c2-4983-ae09-967c269fc828
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DVD_MUA_Coeff, DVD_MUA_Coeff structure [DirectShow], DVD_MUA_CoeffStructure, dshow.dvd_mua_coeff, strmif/DVD_MUA_Coeff, tagDVD_MUA_Coeff
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_MUA_Coeff
product: Windows
targetos: Windows
req.typenames: DVD_MUA_Coeff
req.redist: 
---

# tagDVD_MUA_Coeff structure


## -description



The <code>DVD_MUA_Coeff</code> structure defines the mixing coefficients for one channel in a multichannel audio stream. The <a href="https://msdn.microsoft.com/8aba7e5a-62ec-4ef5-821f-cfef8cf7d93d">DVD_MultichannelAudioAttributes</a> structure contains an array of eight <code>DVD_MUA_Coeff</code> structures, one for each channel in the stream.




## -struct-fields




### -field log2_alpha

The mixing coefficient for this channel to channel 0.
          


### -field log2_beta

The mixing coefficient for this channel to channel 1.
          


## -remarks



The information contained in this structure reflects the mixing coefficients as authored on the digital video disc (DVD). An application cannot modify these values or otherwise use them unless it is also decoding the audio. In the typical DVD filter graph, the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter does not send this information to the decoder.

The alpha coefficient is used to mix to audio channel 0 and the beta coefficient is used to mix to audio channel 1. In general, the following formula calculates the mixing coefficients.


```cpp

Audio channel 0 = coeff[0].alpha * value[0] + coeff[1].alpha * value[1] + ... 
Audio channel 1 = coeff[0].beta * value[0]  + coeff[1].beta * value[1] + ... 

```





## -see-also




<a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a>



<a href="https://msdn.microsoft.com/df830598-f484-483d-a0dc-e6bd9debbe53">DVD_MUA_MixingInfo</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

