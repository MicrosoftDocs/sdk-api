---
UID: NN:audioclient.IAudioCaptureClient
title: IAudioCaptureClient (audioclient.h)
description: The IAudioCaptureClient interface enables a client to read input data from a capture endpoint buffer.
old-location: coreaudio\iaudiocaptureclient.htm
tech.root: CoreAudio
ms.assetid: c0fa6841-56bf-421e-9949-c6a037cf9fd4
ms.date: 12/05/2018
ms.keywords: IAudioCaptureClient, IAudioCaptureClient interface [Core Audio], IAudioCaptureClient interface [Core Audio],described, audioclient/IAudioCaptureClient, coreaudio.iaudiocaptureclient
ms.topic: interface
f1_keywords:
- audioclient/IAudioCaptureClient
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
- IAudioCaptureClient
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioCaptureClient interface


## -description



The <b>IAudioCaptureClient</b> interface enables a client to read input data from a capture endpoint buffer. The client obtains a reference to the <b>IAudioCaptureClient</b> interface on a stream object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioCaptureClient.

The methods in this interface manage the movement of data packets that contain capture data. The length of a data packet is expressed as the number of audio frames in the packet. The size of an audio frame is specified by the <b>nBlockAlign</b> member of the W<b>AVEFORMATEX (or WAVEFORMATEXTENSIBLE)</b> structure that the client obtains by calling the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a> method. The size in bytes of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples. A packet always contains an integral number of audio frames.

When releasing an <b>IAudioCaptureClient</b> interface instance, the client must call the <b>Release</b> method of the instance from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

For a code example that uses the <b>IAudioCaptureClient</b> interface, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioCaptureClient</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioCaptureClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioCaptureClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the next available packet of data in the capture endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize">GetNextPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames in the next data packet in the capture endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases the buffer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a>
 

 

