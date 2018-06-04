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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
Audio channel 0 = coeff[0].alpha * value[0] + coeff[1].alpha * value[1] + ... 
Audio channel 1 = coeff[0].beta * value[0]  + coeff[1].beta * value[1] + ... 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a>



<a href="https://msdn.microsoft.com/df830598-f484-483d-a0dc-e6bd9debbe53">DVD_MUA_MixingInfo</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

