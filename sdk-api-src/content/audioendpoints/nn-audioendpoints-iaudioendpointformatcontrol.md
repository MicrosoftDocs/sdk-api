---
UID: NN:audioendpoints.IAudioEndpointFormatControl
title: IAudioEndpointFormatControl (audioendpoints.h)

description: Used for resetting the current audio endpoint device format.
old-location: coreaudio\iaudioendpointformatcontrol.htm
tech.root: CoreAudio
ms.assetid: 7FF7DCF2-0580-4B50-8EA9-87DB9478B1E8

ms.date: 12/05/2018
ms.keywords: IAudioEndpointFormatControl, IAudioEndpointFormatControl interface [Core Audio], IAudioEndpointFormatControl interface [Core Audio],described, audioendpoints/IAudioEndpointFormatControl, coreaudio.iaudioendpointformatcontrol
ms.topic: interface
f1_keywords: 
 - "audioendpoints/IAudioEndpointFormatControl"
dev_langs:
 - c++
req.header: audioendpoints.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - AudioEndpoints.h
api_name:
 - IAudioEndpointFormatControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointFormatControl interface


## -description


Used for resetting the current audio endpoint device format. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointFormatControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointFormatControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointFormatControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioendpoints/nf-audioendpoints-iaudioendpointformatcontrol-resettodefault">ResetToDefault</a>
</td>
<td align="left" width="63%">
Resets the format to the default setting provided by the device manufacturer.

</td>
</tr>
</table> 


## -remarks



This setting is exposed to the user through the "Sounds" control panel  and can be read from the endpoint property store using
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/pkey-audioengine-deviceformat">PKEY_AudioEngine_DeviceFormat</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
 

 

