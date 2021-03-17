---
UID: NF:xaudio2.IXAudio2SourceVoice.GetFrequencyRatio
title: IXAudio2SourceVoice::GetFrequencyRatio (xaudio2.h)
description: Returns the frequency adjustment ratio of the voice.
helpviewer_keywords: ["GetFrequencyRatio","GetFrequencyRatio method [XAudio2 Audio Mixing APIs]","GetFrequencyRatio method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","GetFrequencyRatio method","IXAudio2SourceVoice.GetFrequencyRatio","IXAudio2SourceVoice::GetFrequencyRatio","xaudio2.ixaudio2sourcevoice_interface_getfrequencyratio","xaudio2/IXAudio2SourceVoice::GetFrequencyRatio"]
old-location: xaudio2\ixaudio2sourcevoice_interface_getfrequencyratio.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.GetFrequencyRatio(float@)
ms.date: 12/05/2018
ms.keywords: GetFrequencyRatio, GetFrequencyRatio method [XAudio2 Audio Mixing APIs], GetFrequencyRatio method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],GetFrequencyRatio method, IXAudio2SourceVoice.GetFrequencyRatio, IXAudio2SourceVoice::GetFrequencyRatio, xaudio2.ixaudio2sourcevoice_interface_getfrequencyratio, xaudio2/IXAudio2SourceVoice::GetFrequencyRatio
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IXAudio2SourceVoice::GetFrequencyRatio
 - xaudio2/IXAudio2SourceVoice::GetFrequencyRatio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2SourceVoice.GetFrequencyRatio
---

# IXAudio2SourceVoice::GetFrequencyRatio


## -description

Returns the frequency adjustment ratio of the voice.

## -parameters

### -param pRatio [out]

Returns the current frequency adjustment ratio if successful.

## -remarks

<b>GetFrequencyRatio</b> always returns the voice's actual current frequency ratio. However, this may not match the ratio set by the most recent <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio">IXAudio2SourceVoice::SetFrequencyRatio</a> call: the actual ratio is only changed the next time the audio engine runs after the <b>IXAudio2SourceVoice::SetFrequencyRatio</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2SourceVoice::SetFrequencyRatio</b> was called with a deferred operation ID).



For information on frequency ratios, see <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio">IXAudio2SourceVoice::SetFrequencyRatio</a>.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>