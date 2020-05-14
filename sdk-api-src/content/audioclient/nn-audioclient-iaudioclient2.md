---
UID: NN:audioclient.IAudioClient2
title: IAudioClient2 (audioclient.h)
description: The IAudioClient2 interface is derived from the IAudioClient interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to do the following:\_opt in for offloading, query stream properties, and get information from the hardware that handles offloading.The audio client can be successful in creating an offloaded stream if the underlying endpoint supports the hardware audio engine, the endpoint has been enumerated and discovered by the audio system, and there are still offload pin instances available on the endpoint.
helpviewer_keywords: ["IAudioClient2","IAudioClient2 interface [Core Audio]","IAudioClient2 interface [Core Audio]","described","audioclient/IAudioClient2","coreaudio.iaudioclient2"]
old-location: coreaudio\iaudioclient2.htm
tech.root: CoreAudio
ms.assetid: 9CE79CEB-115E-4802-A687-B2CB23E6A0E0
ms.date: 12/05/2018
ms.keywords: IAudioClient2, IAudioClient2 interface [Core Audio], IAudioClient2 interface [Core Audio],described, audioclient/IAudioClient2, coreaudio.iaudioclient2
f1_keywords:
- audioclient/IAudioClient2
dev_langs:
- c++
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- Audioclient.h
api_name:
- IAudioClient2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioClient2 interface


## -description


The <b>IAudioClient2</b> interface is derived from the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to do the following: opt in for offloading, query stream properties, and get information from the hardware that handles offloading.The audio client can be successful in creating an offloaded stream if the underlying endpoint supports the hardware audio engine, the endpoint has been enumerated and discovered by the audio system, and there are still offload pin instances available on the endpoint.</p> 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClient2</b> interface inherits from the <a href="https://docs.microsoft.com/en-us/windows/win32/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. <b>IAudioClient2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClient2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-getbuffersizelimits">GetBufferSizeLimits</a>
</td>
<td align="left" width="63%">
Retrieves the buffer size limits of the hardware audio engine in 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-isoffloadcapable">IsOffloadCapable</a>
</td>
<td align="left" width="63%">
Retrieves information about whether or not the endpoint on which a stream is created is capable of supporting an offloaded stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">SetClientProperties</a>
</td>
<td align="left" width="63%">
Sets the properties of the audio stream by populating an <a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties~r1">AudioClientProperties</a> structure.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties~r1">AudioClientProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a>
 

 

