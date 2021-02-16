---
UID: NF:xaudio2.IXAudio2SourceVoice.SetFrequencyRatio
title: IXAudio2SourceVoice::SetFrequencyRatio (xaudio2.h)
description: Sets the frequency adjustment ratio of the voice.
helpviewer_keywords: ["IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","SetFrequencyRatio method","IXAudio2SourceVoice.SetFrequencyRatio","IXAudio2SourceVoice::SetFrequencyRatio","SetFrequencyRatio","SetFrequencyRatio method [XAudio2 Audio Mixing APIs]","SetFrequencyRatio method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","xaudio2.ixaudio2sourcevoice_interface_setfrequencyratio","xaudio2/IXAudio2SourceVoice::SetFrequencyRatio"]
old-location: xaudio2\ixaudio2sourcevoice_interface_setfrequencyratio.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.SetFrequencyRatio(float,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],SetFrequencyRatio method, IXAudio2SourceVoice.SetFrequencyRatio, IXAudio2SourceVoice::SetFrequencyRatio, SetFrequencyRatio, SetFrequencyRatio method [XAudio2 Audio Mixing APIs], SetFrequencyRatio method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, xaudio2.ixaudio2sourcevoice_interface_setfrequencyratio, xaudio2/IXAudio2SourceVoice::SetFrequencyRatio
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
 - IXAudio2SourceVoice::SetFrequencyRatio
 - xaudio2/IXAudio2SourceVoice::SetFrequencyRatio
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
 - IXAudio2SourceVoice.SetFrequencyRatio
---

# IXAudio2SourceVoice::SetFrequencyRatio


## -description

Sets the frequency adjustment ratio of the voice.

## -parameters

### -param Ratio [in]

Frequency adjustment ratio. This value must be between XAUDIO2_MIN_FREQ_RATIO and the <i>MaxFrequencyRatio</i> parameter specified when the voice was created (see <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice">IXAudio2::CreateSourceVoice</a>). XAUDIO2_MIN_FREQ_RATIO currently is 0.0005, which allows pitch to be lowered by up to 11 octaves.

### -param X2DEFAULT

TBD

### -param OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of error codes.

## -remarks

Frequency adjustment is expressed as <i>source frequency</i> / <i>target frequency</i>. Changing the frequency ratio changes the rate audio is played on the voice. A ratio greater than 1.0 will cause the audio to play faster and a ratio less than 1.0 will cause the audio to play slower. Additionally, the frequency ratio affects the pitch of audio on the voice. As an example, a value of 1.0 has no effect on the audio, whereas a value of 2.0 raises pitch by one octave and 0.5 lowers it by one octave.



If <b>SetFrequencyRatio</b> is called specifying a Ratio value outside the valid range, the method will set the frequency ratio to the nearest valid value. A warning also will be generated for debug builds.



<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getfrequencyratio">IXAudio2SourceVoice::GetFrequencyRatio</a> always returns the voice's actual current frequency ratio. However, this may not match the ratio set by the most recent <b>IXAudio2SourceVoice::SetFrequencyRatio</b> call: the actual ratio is only changed the next time the audio engine runs after the <b>IXAudio2SourceVoice::SetFrequencyRatio</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2SourceVoice::SetFrequencyRatio</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--change-voice-pitch">How to: Change Voice Pitch</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>