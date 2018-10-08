---
UID: NN:audioengineendpoint.IAudioEndpointOffloadStreamMeter
title: IAudioEndpointOffloadStreamMeter
author: windows-sdk-content
description: The IAudioEndpointOffloadStreamMeter interface retrieves general information about the audio channels in the offloaded audio stream.
old-location: coreaudio\iaudioendpointoffloadstreammeter.htm
tech.root: CoreAudio
ms.assetid: B19413F9-1DE9-4940-B0A1-11E5278F084B
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IAudioEndpointOffloadStreamMeter, IAudioEndpointOffloadStreamMeter interface [Core Audio], IAudioEndpointOffloadStreamMeter interface [Core Audio],described, audioengineendpoint/IAudioEndpointOffloadStreamMeter, coreaudio.iaudioendpointoffloadstreammeter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointOffloadStreamMeter interface


## -description


The <b>IAudioEndpointOffloadStreamMeter</b> interface retrieves general information about the audio channels in the offloaded audio stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointOffloadStreamMeter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpointOffloadStreamMeter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/52C34D08-8ACD-4E3A-80F4-4FA823E11D9C">GetMeterChannelCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of audio channels in the offloaded stream that can be metered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31F76D5B-D047-4D0E-AA22-DCC1E2E36561">GetMeteringData</a>
</td>
<td align="left" width="63%">
Retrieves general information about the available audio channels in the offloaded stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

