---
UID: NN:mfidl.IMFAudioStreamVolume
title: IMFAudioStreamVolume (mfidl.h)
description: Controls the volume levels of individual audio channels.
helpviewer_keywords: ["IMFAudioStreamVolume","IMFAudioStreamVolume interface [Media Foundation]","IMFAudioStreamVolume interface [Media Foundation]","described","f06ed262-a2ec-4688-b477-877d04cf1892","mf.imfaudiostreamvolume","mfidl/IMFAudioStreamVolume"]
old-location: mf\imfaudiostreamvolume.htm
tech.root: mf
ms.assetid: f06ed262-a2ec-4688-b477-877d04cf1892
ms.date: 12/05/2018
ms.keywords: IMFAudioStreamVolume, IMFAudioStreamVolume interface [Media Foundation], IMFAudioStreamVolume interface [Media Foundation],described, f06ed262-a2ec-4688-b477-877d04cf1892, mf.imfaudiostreamvolume, mfidl/IMFAudioStreamVolume
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
 - IMFAudioStreamVolume
 - mfidl/IMFAudioStreamVolume
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
 - IMFAudioStreamVolume
---

# IMFAudioStreamVolume interface


## -description

Controls the volume levels of individual audio channels.

The streaming audio renderer (SAR) exposes this interface as a service. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier <b>MR_STREAM_VOLUME_SERVICE</b>. You can call <b>GetService</b> directly on the SAR or call it on the Media Session.

## -inheritance

The <b>IMFAudioStreamVolume</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAudioStreamVolume</b> also has these types of members:

## -remarks

If your application does not require channel-level volume control, you can use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume">IMFSimpleAudioVolume</a> interface to control the master volume level of the audio session.

Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). For each channel, the attenuation level is the product of:

<ul>
<li>The master volume level of the audio session.
          </li>
<li>The volume level of the channel.
          </li>
</ul>
For example, if the master volume is 0.8 and the channel volume is 0.5, the attenuation for that channel is 0.8 × 0.5 = 0.4. Volume levels can exceed 1.0 (positive gain), but the audio engine clips any audio samples that exceed zero decibels.

Use the following formula to convert the volume level to the decibel (dB) scale:

Attenuation (dB) = 20 * log10(<i>Level</i>)

For example, a volume level of 0.50 represents 6.02 dB of attenuation.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
