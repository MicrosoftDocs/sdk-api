---
UID: NN:devicetopology.IPerChannelDbLevel
title: IPerChannelDbLevel (devicetopology.h)
description: The IPerChannelDbLevel interface represents a generic subunit control interface that provides per-channel control over the volume level, in decibels, of an audio stream or of a frequency band in an audio stream.
old-location: coreaudio\iperchanneldblevel.htm
tech.root: CoreAudio
ms.assetid: e70b4518-c9de-4426-b8e5-db80656699a9
ms.date: 12/05/2018
ms.keywords: IPerChannelDbLevel, IPerChannelDbLevel interface [Core Audio], IPerChannelDbLevel interface [Core Audio],described, coreaudio.iperchanneldblevel, devicetopology/IPerChannelDbLevel
ms.topic: interface
f1_keywords:
- devicetopology/IPerChannelDbLevel
dev_langs:
- c++
req.header: devicetopology.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Devicetopology.h
api_name:
- IPerChannelDbLevel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPerChannelDbLevel interface


## -description



The <b>IPerChannelDbLevel</b> interface represents a generic subunit control interface that provides per-channel control over the volume level, in decibels, of an audio stream or of a frequency band in an audio stream. A positive volume level represents gain, and a negative value represents attenuation.

Clients do not call the methods in this interface directly. Instead, this interface serves as the base interface for the following interfaces, which clients do call directly:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass Interface</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange Interface</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble Interface</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel Interface</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPerChannelDbLevel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPerChannelDbLevel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPerChannelDbLevel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">GetChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">GetLevel</a>
</td>
<td align="left" width="63%">
Gets the volume level, in decibels, of the specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevelrange">GetLevelRange</a>
</td>
<td align="left" width="63%">
Gets the range, in decibels, of the volume level of the specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-setlevel">SetLevel</a>
</td>
<td align="left" width="63%">
Sets the volume level, in decibels, of the specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-setlevelallchannels">SetLevelAllChannels</a>
</td>
<td align="left" width="63%">
Sets the volume levels, in decibels, of all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-setleveluniform">SetLevelUniform</a>
</td>
<td align="left" width="63%">
Sets all channels in the audio stream to the same uniform volume level, in decibels.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel Interface</a>
 

 

