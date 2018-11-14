---
UID: NN:devicetopology.IPerChannelDbLevel
title: IPerChannelDbLevel
author: windows-sdk-content
description: The IPerChannelDbLevel interface represents a generic subunit control interface that provides per-channel control over the volume level, in decibels, of an audio stream or of a frequency band in an audio stream.
old-location: coreaudio\iperchanneldblevel.htm
tech.root: CoreAudio
ms.assetid: e70b4518-c9de-4426-b8e5-db80656699a9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPerChannelDbLevel, IPerChannelDbLevel interface [Core Audio], IPerChannelDbLevel interface [Core Audio],described, coreaudio.iperchanneldblevel, devicetopology/IPerChannelDbLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPerChannelDbLevel interface


## -description



The <b>IPerChannelDbLevel</b> interface represents a generic subunit control interface that provides per-channel control over the volume level, in decibels, of an audio stream or of a frequency band in an audio stream. A positive volume level represents gain, and a negative value represents attenuation.

Clients do not call the methods in this interface directly. Instead, this interface serves as the base interface for the following interfaces, which clients do call directly:

<ul>
<li>
<a href="https://msdn.microsoft.com/036ca996-8612-4905-9afa-a4c3b4624652">IAudioBass Interface</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d2d93dba-1867-4c3a-9cd1-60842bf8311d">IAudioMidrange Interface</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ace174e-c21c-41e7-9830-80d247d8437f">IAudioTreble Interface</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e7d7111-e4b0-43b3-af35-9878d1a19e5f">IAudioVolumeLevel Interface</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPerChannelDbLevel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPerChannelDbLevel</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">GetChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">GetLevel</a>
</td>
<td align="left" width="63%">
Gets the volume level, in decibels, of the specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/492eddb0-f8f2-4639-b5fe-1d02bf8c983a">GetLevelRange</a>
</td>
<td align="left" width="63%">
Gets the range, in decibels, of the volume level of the specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/103efe46-bca5-40a7-815b-d2a1f6e29cbc">SetLevel</a>
</td>
<td align="left" width="63%">
Sets the volume level, in decibels, of the specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92c06b38-954d-4bab-b4ea-0f30e64aa9e4">SetLevelAllChannels</a>
</td>
<td align="left" width="63%">
Sets the volume levels, in decibels, of all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b78bebcb-d32b-4eda-a805-35d4459b6b4f">SetLevelUniform</a>
</td>
<td align="left" width="63%">
Sets all channels in the audio stream to the same uniform volume level, in decibels.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/036ca996-8612-4905-9afa-a4c3b4624652">IAudioBass Interface</a>



<a href="https://msdn.microsoft.com/d2d93dba-1867-4c3a-9cd1-60842bf8311d">IAudioMidrange Interface</a>



<a href="https://msdn.microsoft.com/3ace174e-c21c-41e7-9830-80d247d8437f">IAudioTreble Interface</a>



<a href="https://msdn.microsoft.com/5e7d7111-e4b0-43b3-af35-9878d1a19e5f">IAudioVolumeLevel Interface</a>
 

 

