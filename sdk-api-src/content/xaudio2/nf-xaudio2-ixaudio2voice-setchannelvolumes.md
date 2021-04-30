---
UID: NF:xaudio2.IXAudio2Voice.SetChannelVolumes
title: IXAudio2Voice::SetChannelVolumes (xaudio2.h)
description: Sets the volume levels for the voice, per channel.
helpviewer_keywords: ["IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","SetChannelVolumes method","IXAudio2Voice.SetChannelVolumes","IXAudio2Voice::SetChannelVolumes","SetChannelVolumes","SetChannelVolumes method [XAudio2 Audio Mixing APIs]","SetChannelVolumes method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","xaudio2.ixaudio2voice_interface_setchannelvolumes","xaudio2/IXAudio2Voice::SetChannelVolumes"]
old-location: xaudio2\ixaudio2voice_interface_setchannelvolumes.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetChannelVolumes(UINT32,const float,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetChannelVolumes method, IXAudio2Voice.SetChannelVolumes, IXAudio2Voice::SetChannelVolumes, SetChannelVolumes, SetChannelVolumes method [XAudio2 Audio Mixing APIs], SetChannelVolumes method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_setchannelvolumes, xaudio2/IXAudio2Voice::SetChannelVolumes
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
 - IXAudio2Voice::SetChannelVolumes
 - xaudio2/IXAudio2Voice::SetChannelVolumes
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
 - IXAudio2Voice.SetChannelVolumes
---

# IXAudio2Voice::SetChannelVolumes


## -description

Sets the volume levels for the voice, per channel.

## -parameters

### -param Channels [in]

Number of channels in the voice.

### -param pVolumes [in]

Array containing the new volumes of each channel in the voice. The array must have <i>Channels</i> elements. See Remarks for more information on volume levels.

### -param X2DEFAULT

TBD

### -param OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

<b>SetChannelVolumes</b> controls a voice's per-channel output levels and is applied just after the voice's final SRC and before its sends.



This method is valid only for source and submix voices, because mastering voices do not specify volume per channel.



Volume levels are expressed as floating-point amplitude multipliers between -XAUDIO2_MAX_VOLUME_LEVEL and XAUDIO2_MAX_VOLUME_LEVEL (-2²⁴ to 2²⁴), with a maximum gain of 144.5 dB. A volume of 1 means there is no attenuation or gain and 0 means silence. Negative levels can be used to invert the audio's phase. See <a href="/windows/desktop/xaudio2/xaudio2-volume-and-pitch-control">XAudio2 Volume and Pitch Control</a> for additional information on volume control.



<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-getchannelvolumes">IXAudio2Voice::GetChannelVolumes</a> always returns the volume levels most recently set by <b>IXAudio2Voice::SetChannelVolumes</b>. However, those values may not actually be in effect yet: they only take effect the next time the audio engine runs after the <b>IXAudio2Voice::SetChannelVolumes</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetChannelVolumes</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--change-voice-volume">How to: Change Voice Volume</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>