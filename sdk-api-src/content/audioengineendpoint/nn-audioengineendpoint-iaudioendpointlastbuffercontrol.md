---
UID: NN:audioengineendpoint.IAudioEndpointLastBufferControl
title: IAudioEndpointLastBufferControl (audioengineendpoint.h)
description: Provides functionality to allow an offload stream client to notify the endpoint that the last buffer has been sent only partially filled.helpviewer_keywords: ["IAudioEndpointLastBufferControl","IAudioEndpointLastBufferControl interface [Core Audio]","IAudioEndpointLastBufferControl interface [Core Audio]","described","audioengineendpoint/IAudioEndpointLastBufferControl","coreaudio.iaudioendpointlastbuffercontrol"]
old-location: coreaudio\iaudioendpointlastbuffercontrol.htm
tech.root: CoreAudio
ms.assetid: 79f4b370-fd04-41a9-ad74-54f7edd084c2
ms.date: 12/05/2018
ms.keywords: IAudioEndpointLastBufferControl, IAudioEndpointLastBufferControl interface [Core Audio], IAudioEndpointLastBufferControl interface [Core Audio],described, audioengineendpoint/IAudioEndpointLastBufferControl, coreaudio.iaudioendpointlastbuffercontrol
f1_keywords:
- audioengineendpoint/IAudioEndpointLastBufferControl
dev_langs:
- c++
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AudioEngineEndpoint.idl
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
- IAudioEndpointLastBufferControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointLastBufferControl interface


## -description


Provides functionality to allow an offload stream client to notify  the endpoint that the last buffer has been sent only partially filled.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointLastBufferControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointLastBufferControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointLastBufferControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointlastbuffercontrol-islastbuffercontrolsupported">IsLastBufferControlSupported</a>
</td>
<td align="left" width="63%">
Indicates if last buffer control is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointlastbuffercontrol-releaseoutputdatapointerforlastbuffer">ReleaseOutputDataPointerForLastBuffer</a>
</td>
<td align="left" width="63%">
Releases the output data pointer for the last buffer.

</td>
</tr>
</table> 


## -remarks



This is an optional interface on an endpoint.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
 

 

