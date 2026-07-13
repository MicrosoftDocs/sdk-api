---
UID: NN:endpointvolume.IAudioEndpointVolumeEx
title: IAudioEndpointVolumeEx (endpointvolume.h)
description: The IAudioEndpointVolumeEx interface provides volume controls on the audio stream to or from a device endpoint.
helpviewer_keywords: ["IAudioEndpointVolumeEx","IAudioEndpointVolumeEx interface [Core Audio]","IAudioEndpointVolumeEx interface [Core Audio]","described","coreaudio.iaudioendpointvolumeex","endpointvolume/IAudioEndpointVolumeEx"]
old-location: coreaudio\iaudioendpointvolumeex.htm
tech.root: CoreAudio
ms.assetid: 905ef0c9-ac32-4dfd-a25a-820cafa04815
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolumeEx, IAudioEndpointVolumeEx interface [Core Audio], IAudioEndpointVolumeEx interface [Core Audio],described, coreaudio.iaudioendpointvolumeex, endpointvolume/IAudioEndpointVolumeEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointVolumeEx
 - endpointvolume/IAudioEndpointVolumeEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolumeEx
---

# IAudioEndpointVolumeEx interface


## -description

The <b>IAudioEndpointVolumeEx</b> interface provides volume controls on the audio stream to or from a device endpoint.

A client obtains a reference to the <b>IAudioEndpointVolumeEx</b> interface of an endpoint device by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioEndpointVolumeEx.

## -inheritance

The <b>IAudioEndpointVolumeEx</b> interface inherits from <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a>. <b>IAudioEndpointVolumeEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>
