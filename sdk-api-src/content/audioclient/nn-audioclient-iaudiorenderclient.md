---
UID: NN:audioclient.IAudioRenderClient
title: IAudioRenderClient (audioclient.h)
description: The IAudioRenderClient interface enables a client to write output data to a rendering endpoint buffer.
helpviewer_keywords: ["IAudioRenderClient","IAudioRenderClient interface [Core Audio]","IAudioRenderClient interface [Core Audio]","described","audioclient/IAudioRenderClient","coreaudio.iaudiorenderclient"]
old-location: coreaudio\iaudiorenderclient.htm
tech.root: CoreAudio
ms.assetid: e3e18e1e-1a09-4072-add6-36d2a6428a74
ms.date: 12/05/2018
ms.keywords: IAudioRenderClient, IAudioRenderClient interface [Core Audio], IAudioRenderClient interface [Core Audio],described, audioclient/IAudioRenderClient, coreaudio.iaudiorenderclient
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
 - IAudioRenderClient
 - audioclient/IAudioRenderClient
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
 - IAudioRenderClient
---

# IAudioRenderClient interface


## -description

The <b>IAudioRenderClient</b> interface enables a client to write output data to a rendering endpoint buffer. The client obtains a reference to the <b>IAudioRenderClient</b> interface of a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_IAudioRenderClient.

The methods in this interface manage the movement of data packets that contain audio-rendering data. The length of a data packet is expressed as the number of audio frames in the packet. The size of an audio frame is specified by the <b>nBlockAlign</b> member of the <b>WAVEFORMATEX</b> structure that the client obtains by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a> method. The size in bytes of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples. A packet always contains an integral number of audio frames.

When releasing an <b>IAudioRenderClient</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

For code examples that use the <b>IAudioRenderClient</b> interface, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/exclusive-mode-streams">Exclusive-Mode Streams</a>
</li>
</ul>

## -inheritance

The <b>IAudioRenderClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioRenderClient</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
