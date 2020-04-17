---
UID: NN:audioengineendpoint.IAudioEndpointOffloadStreamMeter
title: IAudioEndpointOffloadStreamMeter (audioengineendpoint.h)
description: The IAudioEndpointOffloadStreamMeter interface retrieves general information about the audio channels in the offloaded audio stream.helpviewer_keywords: ["IAudioEndpointOffloadStreamMeter","IAudioEndpointOffloadStreamMeter interface [Core Audio]","IAudioEndpointOffloadStreamMeter interface [Core Audio]","described","audioengineendpoint/IAudioEndpointOffloadStreamMeter","coreaudio.iaudioendpointoffloadstreammeter"]
old-location: coreaudio\iaudioendpointoffloadstreammeter.htm
tech.root: CoreAudio
ms.assetid: B19413F9-1DE9-4940-B0A1-11E5278F084B
ms.date: 12/05/2018
ms.keywords: IAudioEndpointOffloadStreamMeter, IAudioEndpointOffloadStreamMeter interface [Core Audio], IAudioEndpointOffloadStreamMeter interface [Core Audio],described, audioengineendpoint/IAudioEndpointOffloadStreamMeter, coreaudio.iaudioendpointoffloadstreammeter
f1_keywords:
- audioengineendpoint/IAudioEndpointOffloadStreamMeter
dev_langs:
- c++
req.header: audioengineendpoint.h
req.include-header: 
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
- COM
api_location:
- audioengineendpoint.h
api_name:
- IAudioEndpointOffloadStreamMeter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointOffloadStreamMeter interface


## -description


The <b>IAudioEndpointOffloadStreamMeter</b> interface retrieves general information about the audio channels in the offloaded audio stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointOffloadStreamMeter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointOffloadStreamMeter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointOffloadStreamMeter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreammeter-getmeterchannelcount">GetMeterChannelCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of audio channels in the offloaded stream that can be metered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreammeter-getmeteringdata">GetMeteringData</a>
</td>
<td align="left" width="63%">
Retrieves general information about the available audio channels in the offloaded stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
 

 

