---
UID: NN:endpointvolume.IAudioEndpointVolumeEx
title: IAudioEndpointVolumeEx (endpointvolume.h)
author: windows-sdk-content
description: The IAudioEndpointVolumeEx interface provides volume controls on the audio stream to or from a device endpoint.
old-location: coreaudio\iaudioendpointvolumeex.htm
tech.root: CoreAudio
ms.assetid: 905ef0c9-ac32-4dfd-a25a-820cafa04815
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolumeEx, IAudioEndpointVolumeEx interface [Core Audio], IAudioEndpointVolumeEx interface [Core Audio],described, coreaudio.iaudioendpointvolumeex, endpointvolume/IAudioEndpointVolumeEx
ms.topic: interface
f1_keywords: 
 - "endpointvolume/IAudioEndpointVolumeEx"
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolumeEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointVolumeEx interface


## -description


The <b>IAudioEndpointVolumeEx</b> interface provides volume controls on the audio stream to or from a device endpoint.

A client obtains a reference to the <b>IAudioEndpointVolumeEx</b> interface of an endpoint device by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioEndpointVolumeEx.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointVolumeEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a>. <b>IAudioEndpointVolumeEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointVolumeEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumeex-getvolumerangechannel">GetVolumeRangeChannel</a>
</td>
<td align="left" width="63%">
Gets the volume range for a specified channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>
 

 

