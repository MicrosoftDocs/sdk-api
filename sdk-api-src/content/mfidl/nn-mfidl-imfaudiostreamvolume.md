---
UID: NN:mfidl.IMFAudioStreamVolume
title: IMFAudioStreamVolume
author: windows-sdk-content
description: Controls the volume levels of individual audio channels.
old-location: mf\imfaudiostreamvolume.htm
old-project: medfound
ms.assetid: f06ed262-a2ec-4688-b477-877d04cf1892
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFAudioStreamVolume, IMFAudioStreamVolume interface [Media Foundation], IMFAudioStreamVolume interface [Media Foundation],described, f06ed262-a2ec-4688-b477-877d04cf1892, mf.imfaudiostreamvolume, mfidl/IMFAudioStreamVolume
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioStreamVolume
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFAudioStreamVolume interface


## -description


Controls the volume levels of individual audio channels.

The streaming audio renderer (SAR) exposes this interface as a service. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier <b>MR_STREAM_VOLUME_SERVICE</b>. You can call <b>GetService</b> directly on the SAR or call it on the Media Session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAudioStreamVolume</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFAudioStreamVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAudioStreamVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbcc0b5b-a60d-49ca-8b1c-7104e039a7d2">GetAllVolumes</a>
</td>
<td align="left" width="63%">
Retrieves the volume levels for all of the channels in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d19a56db-cd5f-4a19-98f0-42327c259b01">GetChannelCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of channels in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cfcc3a8-2911-45a3-8322-bf4e3b023dd2">GetChannelVolume</a>
</td>
<td align="left" width="63%">
Retrieves the volume level for a specified channel in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c278693-5a2f-4aa2-b477-3b3014b2cc89">SetAllVolumes</a>
</td>
<td align="left" width="63%">
Sets the individual volume levels for all of the channels in the audio stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7786a6aa-c777-4b65-b38c-a75cd654a080">SetChannelVolume</a>
</td>
<td align="left" width="63%">
Sets the volume level for a specified channel in the audio stream.
        

</td>
</tr>
</table> 


## -remarks



If your application does not require channel-level volume control, you can use the <a href="https://msdn.microsoft.com/002d85a7-8bc3-422e-8ced-1907ac121d7b">IMFSimpleAudioVolume</a> interface to control the master volume level of the audio session.

Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). For each channel, the attenuation level is the product of:

<ul>
<li>The master volume level of the audio session.
          </li>
<li>The volume level of the channel.
          </li>
</ul>
For example, if the master volume is 0.8 and the channel volume is 0.5, the attenuation for that channel is 0.8 × 0.5 = 0.4. Volume levels can exceed 1.0 (positive gain), but the audio engine clips any audio samples that exceed zero decibels.

Use the following formula to convert the volume level to the decibel (dB) scale:

Attenuation (dB) = 20 * log10(<i>Level</i>)

For example, a volume level of 0.50 represents 6.02 dB of attenuation.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

