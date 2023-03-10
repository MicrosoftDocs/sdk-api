---
UID: NN:audioclient.IAudioCaptureClient
title: IAudioCaptureClient (audioclient.h)
description: The IAudioCaptureClient interface enables a client to read input data from a capture endpoint buffer.
helpviewer_keywords: ["IAudioCaptureClient","IAudioCaptureClient interface [Core Audio]","IAudioCaptureClient interface [Core Audio]","described","audioclient/IAudioCaptureClient","coreaudio.iaudiocaptureclient"]
old-location: coreaudio\iaudiocaptureclient.htm
tech.root: CoreAudio
ms.assetid: c0fa6841-56bf-421e-9949-c6a037cf9fd4
ms.date: 12/05/2018
ms.keywords: IAudioCaptureClient, IAudioCaptureClient interface [Core Audio], IAudioCaptureClient interface [Core Audio],described, audioclient/IAudioCaptureClient, coreaudio.iaudiocaptureclient
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioCaptureClient
 - audioclient/IAudioCaptureClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioCaptureClient
---

# IAudioCaptureClient interface


## -description

The <b>IAudioCaptureClient</b> interface enables a client to read input data from a capture endpoint buffer. The client obtains a reference to the <b>IAudioCaptureClient</b> interface on a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioCaptureClient.

The methods in this interface manage the movement of data packets that contain capture data. The length of a data packet is expressed as the number of audio frames in the packet. The size of an audio frame is specified by the <b>nBlockAlign</b> member of the <b>WAVEFORMATEX (or WAVEFORMATEXTENSIBLE)</b> structure that the client obtains by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a> method. The size in bytes of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples. A packet always contains an integral number of audio frames.

When releasing an <b>IAudioCaptureClient</b> interface instance, the client must call the <b>Release</b> method of the instance from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

For a code example that uses the <b>IAudioCaptureClient</b> interface, see <a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>.

## -inheritance

The <b>IAudioCaptureClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioCaptureClient</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
