---
UID: NN:audioengineendpoint.IAudioEndpointOffloadStreamVolume
title: IAudioEndpointOffloadStreamVolume
author: windows-sdk-content
description: The IAudioEndpointOffloadStreamVolume interface allows the client application to manipulate the volume level of the offloaded audio stream.
old-location: coreaudio\iaudioendpointoffloadstreamvolume.htm
tech.root: CoreAudio
ms.assetid: 73FD2289-8414-4A63-A518-634D6F2DF48D
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAudioEndpointOffloadStreamVolume, IAudioEndpointOffloadStreamVolume interface [Core Audio], IAudioEndpointOffloadStreamVolume interface [Core Audio],described, audioengineendpoint/IAudioEndpointOffloadStreamVolume, coreaudio.iaudioendpointoffloadstreamvolume
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAudioEndpointOffloadStreamVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointOffloadStreamVolume interface


## -description


The <b>IAudioEndpointOffloadStreamVolume</b> interface allows the client application to manipulate the volume level of the offloaded audio stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointOffloadStreamVolume</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpointOffloadStreamVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointOffloadStreamVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B15CA88E-EDB3-4BB4-9B74-98BB1D0CE288">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Retrieves the volume levels for the various audio channels in the offloaded stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/361E3B06-D543-4C86-BE0E-E3E0E2A51A27">GetVolumeChannelCount</a>
</td>
<td align="left" width="63%">
Returns the number of available audio channels in the offloaded stream for which the volume levels can be manipulated by the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80E736B5-AF8E-46B3-9CDF-753B045F60D9">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the various audio channels in the offloaded stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

