---
UID: NN:audioclient.IAudioClock
title: IAudioClock (audioclient.h)
description: The IAudioClock interface enables a client to monitor a stream's data rate and the current position in the stream.
old-location: coreaudio\iaudioclock.htm
tech.root: CoreAudio
ms.assetid: dbec9468-b555-42a0-a988-dec3a66c9f96
ms.date: 12/05/2018
ms.keywords: IAudioClock, IAudioClock interface [Core Audio], IAudioClock interface [Core Audio],described, audioclient/IAudioClock, coreaudio.iaudioclock
f1_keywords:
- audioclient/IAudioClock
dev_langs:
- c++
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- IAudioClock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioClock interface


## -description



The <b>IAudioClock</b> interface enables a client to monitor a stream's data rate and the current position in the stream. The client obtains a reference to the <b>IAudioClock</b> interface of a stream object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClock.

When releasing an <b>IAudioClock</b> interface instance, the client must call the interface's Release method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getcharacteristics">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getfrequency">GetFrequency</a>
</td>
<td align="left" width="63%">
Gets the device frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getposition">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the current position in the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a>
 

 

