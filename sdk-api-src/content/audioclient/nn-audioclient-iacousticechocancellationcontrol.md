---
UID: NN:audioclient.IAcousticEchoCancellationControl
tech.root: CoreAudio
title: IAcousticEchoCancellationControl
ms.date: 02/28/2023
targetos: Windows
description: Provides a mechanism for determining if an audio capture endpoint supports acoustic echo cancellation (AEC) and, if so, allows the client to set the audio render endpoint that should be used as the reference stream. 
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioclient.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22621
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAcousticEchoCancellationControl
f1_keywords:
 - IAcousticEchoCancellationControl
 - audioclient/IAcousticEchoCancellationControl
dev_langs:
 - c++
helpviewer_keywords:
 - IAcousticEchoCancellationControl
---

## -description

Provides a mechanism for determining if an audio capture endpoint supports acoustic echo cancellation (AEC) and, if so, allows the client to set the audio render endpoint that should be used as the reference stream.  

## -remarks

The following example illustrates the usage of **IAcousticEchoCancellationControl** interface. Call [IAudioClient::GetService](./nf-audioclient-iaudioclient-getservice.md), passing in the IID for the **IAcousticEchoCancellationControl** interface. If it succeeds, the capture endpoint supports control of the loopback reference endpoint for AEC. Note that an endpoint may support AEC, but may not support control of loopback reference endpoint for AEC. Call [SetEchoCancellationRenderEndpoint](./nf-audioclient-iacousticechocancellationcontrol-setechocancellationrenderendpoint.md) to set the reference stream for AEC. If the call to **GetService** fails with **E_NOINTERFACE**, then the AEC effect on the endpoint (if supported), does not allow control over the loopback reference endpoint.

```cpp
wil::com_ptr_nothrow<IAudioClient> audioClient;

RETURN_IF_FAILED(device->Activate(_uuidof(IAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void **)&audioClient));

// Call Initialize before calling GetService
// Implementation of IAudioClient::Initialize has been omitted from this sample for brevity.

RETURN_IF_FAILED(audioClient->Initialize(…));

// If the capture endpoint supports acoustic echo cancellation (AEC), pass it the endpoint id of the
// audio render endpoint that should be used as the reference stream. If the capture endpoint does not
// support AEC, the GetService call fails with E_NOINTERFACE, so errors from GetService are not
// treated as fatal.

wil::com_ptr_nothrow<IAcousticEchoCancellationControl> audioAcousticEchoCancellationControl;

if (SUCCEEDED(audioClient->GetService(IID_PPV_ARGS(&audioAcousticEchoCancellationControl))))
{

RETURN_IF_FAILED(audioAcousticEchoCancellationControl-> SetEchoCancellationRenderEndpoint(endpointIdOfReferenceAudioStream));

}
```

## -see-also

