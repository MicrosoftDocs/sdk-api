---
UID: NN:audioclient.IAudioClient
title: IAudioClient (audioclient.h)
description: The IAudioClient interface enables a client to create and initialize an audio stream between an audio application and the audio engine (for a shared-mode stream) or the hardware buffer of an audio endpoint device (for an exclusive-mode stream).
helpviewer_keywords: ["IAudioClient","IAudioClient interface [Core Audio]","IAudioClient interface [Core Audio]","described","audioclient/IAudioClient","coreaudio.iaudioclient"]
old-location: coreaudio\iaudioclient.htm
tech.root: CoreAudio
ms.assetid: 5088a3f1-5001-4ed9-a495-9e91df613ab0
ms.date: 12/05/2018
ms.keywords: IAudioClient, IAudioClient interface [Core Audio], IAudioClient interface [Core Audio],described, audioclient/IAudioClient, coreaudio.iaudioclient
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
 - IAudioClient
 - audioclient/IAudioClient
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
 - IAudioClient
---

# IAudioClient interface


## -description

The <b>IAudioClient</b> interface enables a client to create and initialize an audio stream between an audio application and the audio engine (for a shared-mode stream) or the hardware buffer of an <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint device</a> (for an exclusive-mode stream). A client obtains a reference to an <b>IAudioClient</b> interface for an audio endpoint device by following these steps:<ol>
<li>By using one of the techniques described in <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device.</li>
<li>Call the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioClient. Starting in Windows 10 Build 20348 callers can pass an <a href="../audioclientactivationparams/ns-audioclientactivationparams-audioclient_activation_params.md">AUDIOCLIENT_ACTIVATION_PARAMS</a> to configure the <b>IAudioClient</b> for loopback capture with a process filter.</li>
</ol>


The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.

For code examples that use the <b>IAudioClient</b> interface, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/exclusive-mode-streams">Exclusive-Mode Streams</a>
</li>
</ul>

## -inheritance

The <b>IAudioClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClient</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  In Windows 8, the first use of <b>IAudioClient</b> to access the audio device should be on the STA thread. Calls from an MTA thread may result in undefined behavior.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
