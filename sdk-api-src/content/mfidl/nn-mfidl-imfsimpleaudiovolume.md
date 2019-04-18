---
UID: NN:mfidl.IMFSimpleAudioVolume
title: IMFSimpleAudioVolume (mfidl.h)
author: windows-sdk-content
description: Controls the master volume level of the audio session associated with the streaming audio renderer (SAR) and the audio capture source.
old-location: mf\imfsimpleaudiovolume.htm
tech.root: medfound
ms.assetid: 002d85a7-8bc3-422e-8ced-1907ac121d7b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 002d85a7-8bc3-422e-8ced-1907ac121d7b, IMFSimpleAudioVolume, IMFSimpleAudioVolume interface [Media Foundation], IMFSimpleAudioVolume interface [Media Foundation],described, mf.imfsimpleaudiovolume, mfidl/IMFSimpleAudioVolume
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSimpleAudioVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSimpleAudioVolume interface


## -description


Controls the master volume level of the audio session associated with the streaming audio renderer (SAR) and the audio capture source.

The SAR and the audio capture source expose this interface as a service. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. For the SAR, use the service identifier MR_POLICY_VOLUME_SERVICE. For the audio capture source, use the service identifier MR_CAPTURE_POLICY_VOLUME_SERVICE.  You can call <b>GetService</b> directly on the SAR or the audio capture source, or call it on the Media Session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSimpleAudioVolume</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSimpleAudioVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSimpleAudioVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03ce097e-c4e5-4dac-84c0-b569efc420bc">GetMasterVolume</a>
</td>
<td align="left" width="63%">
Retrieves the master volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13907d3c-62c0-4cb8-8921-5a38a63d7d6e">GetMute</a>
</td>
<td align="left" width="63%">
Queries whether the audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42b51817-3c2a-463a-a533-19c327c57354">SetMasterVolume</a>
</td>
<td align="left" width="63%">
Sets the master volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8840d15-d4d5-481e-9002-54fdbf323c9c">SetMute</a>
</td>
<td align="left" width="63%">
Mutes or unmutes the audio.

</td>
</tr>
</table> 


## -remarks



To control the volume levels of individual channels, use the <a href="https://msdn.microsoft.com/f06ed262-a2ec-4688-b477-877d04cf1892">IMFAudioStreamVolume</a> interface. The <b>IMFAudioStreamVolume</b>   interface is supported by the SAR only.

Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). For each channel, the attenuation level is the product of:

<ul>
<li>
The master volume level of the audio session.

</li>
<li>
The volume level of the channel.

</li>
</ul>
For example, if the master volume is 0.8 and the channel volume is 0.5, the attenuaton for that channel is 0.8 × 0.5 = 0.4. Volume levels can exceed 1.0 (positive gain), but the audio engine clips any audio samples that exceed zero decibels. To change the volume level of individual channels, use the <a href="https://msdn.microsoft.com/f06ed262-a2ec-4688-b477-877d04cf1892">IMFAudioStreamVolume</a> interface.

Use the following formula to convert the volume level to the decibel (dB) scale:

Attenuation (dB) = 20 * log10(<i>Level</i>)
        

For example, a volume level of 0.50 represents 6.02 dB of attenuation.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

