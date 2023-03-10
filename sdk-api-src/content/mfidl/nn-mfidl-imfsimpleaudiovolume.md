---
UID: NN:mfidl.IMFSimpleAudioVolume
title: IMFSimpleAudioVolume (mfidl.h)
description: Controls the master volume level of the audio session associated with the streaming audio renderer (SAR) and the audio capture source.
helpviewer_keywords: ["002d85a7-8bc3-422e-8ced-1907ac121d7b","IMFSimpleAudioVolume","IMFSimpleAudioVolume interface [Media Foundation]","IMFSimpleAudioVolume interface [Media Foundation]","described","mf.imfsimpleaudiovolume","mfidl/IMFSimpleAudioVolume"]
old-location: mf\imfsimpleaudiovolume.htm
tech.root: mf
ms.assetid: 002d85a7-8bc3-422e-8ced-1907ac121d7b
ms.date: 12/05/2018
ms.keywords: 002d85a7-8bc3-422e-8ced-1907ac121d7b, IMFSimpleAudioVolume, IMFSimpleAudioVolume interface [Media Foundation], IMFSimpleAudioVolume interface [Media Foundation],described, mf.imfsimpleaudiovolume, mfidl/IMFSimpleAudioVolume
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSimpleAudioVolume
 - mfidl/IMFSimpleAudioVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSimpleAudioVolume
---

# IMFSimpleAudioVolume interface


## -description

Controls the master volume level of the audio session associated with the streaming audio renderer (SAR) and the audio capture source.

The SAR and the audio capture source expose this interface as a service. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. For the SAR, use the service identifier MR_POLICY_VOLUME_SERVICE. For the audio capture source, use the service identifier MR_CAPTURE_POLICY_VOLUME_SERVICE.  You can call <b>GetService</b> directly on the SAR or the audio capture source, or call it on the Media Session.

## -inheritance

The <b>IMFSimpleAudioVolume</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSimpleAudioVolume</b> also has these types of members:

## -remarks

To control the volume levels of individual channels, use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume">IMFAudioStreamVolume</a> interface. The <b>IMFAudioStreamVolume</b>   interface is supported by the SAR only.

Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). For each channel, the attenuation level is the product of:

<ul>
<li>
The master volume level of the audio session.

</li>
<li>
The volume level of the channel.

</li>
</ul>
For example, if the master volume is 0.8 and the channel volume is 0.5, the attenuation for that channel is 0.8 × 0.5 = 0.4. Volume levels can exceed 1.0 (positive gain), but the audio engine clips any audio samples that exceed zero decibels. To change the volume level of individual channels, use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume">IMFAudioStreamVolume</a> interface.

Use the following formula to convert the volume level to the decibel (dB) scale:

Attenuation (dB) = 20 * log10(<i>Level</i>)
        

For example, a volume level of 0.50 represents 6.02 dB of attenuation.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
