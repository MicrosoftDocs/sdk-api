---
UID: NN:audioengineendpoint.IAudioEndpointOffloadStreamVolume
title: IAudioEndpointOffloadStreamVolume (audioengineendpoint.h)
description: The IAudioEndpointOffloadStreamVolume interface allows the client application to manipulate the volume level of the offloaded audio stream.
helpviewer_keywords: ["IAudioEndpointOffloadStreamVolume","IAudioEndpointOffloadStreamVolume interface [Core Audio]","IAudioEndpointOffloadStreamVolume interface [Core Audio]","described","audioengineendpoint/IAudioEndpointOffloadStreamVolume","coreaudio.iaudioendpointoffloadstreamvolume"]
old-location: coreaudio\iaudioendpointoffloadstreamvolume.htm
tech.root: CoreAudio
ms.assetid: 73FD2289-8414-4A63-A518-634D6F2DF48D
ms.date: 12/05/2018
ms.keywords: IAudioEndpointOffloadStreamVolume, IAudioEndpointOffloadStreamVolume interface [Core Audio], IAudioEndpointOffloadStreamVolume interface [Core Audio],described, audioengineendpoint/IAudioEndpointOffloadStreamVolume, coreaudio.iaudioendpointoffloadstreamvolume
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointOffloadStreamVolume
 - audioengineendpoint/IAudioEndpointOffloadStreamVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamVolume
---

# IAudioEndpointOffloadStreamVolume interface


## -description

The <b>IAudioEndpointOffloadStreamVolume</b> interface allows the client application to manipulate the volume level of the offloaded audio stream.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointOffloadStreamVolume</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointOffloadStreamVolume</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreamvolume-getchannelvolumes">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Retrieves the volume levels for the various audio channels in the offloaded stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreamvolume-getvolumechannelcount">GetVolumeChannelCount</a>
</td>
<td align="left" width="63%">
Returns the number of available audio channels in the offloaded stream for which the volume levels can be manipulated by the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreamvolume-setchannelvolumes">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the various audio channels in the offloaded stream.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>

