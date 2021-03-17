---
UID: NF:xaudio2.IXAudio2Voice.GetChannelVolumes
title: IXAudio2Voice::GetChannelVolumes (xaudio2.h)
description: Returns the volume levels for the voice, per channel.
helpviewer_keywords: ["GetChannelVolumes","GetChannelVolumes method [XAudio2 Audio Mixing APIs]","GetChannelVolumes method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","GetChannelVolumes method","IXAudio2Voice.GetChannelVolumes","IXAudio2Voice::GetChannelVolumes","xaudio2.ixaudio2voice_interface_getchannelvolumes","xaudio2/IXAudio2Voice::GetChannelVolumes"]
old-location: xaudio2\ixaudio2voice_interface_getchannelvolumes.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetChannelVolumes(UINT32,float@)
ms.date: 12/05/2018
ms.keywords: GetChannelVolumes, GetChannelVolumes method [XAudio2 Audio Mixing APIs], GetChannelVolumes method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetChannelVolumes method, IXAudio2Voice.GetChannelVolumes, IXAudio2Voice::GetChannelVolumes, xaudio2.ixaudio2voice_interface_getchannelvolumes, xaudio2/IXAudio2Voice::GetChannelVolumes
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
 - IXAudio2Voice::GetChannelVolumes
 - xaudio2/IXAudio2Voice::GetChannelVolumes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAudio2.h
api_name:
 - IXAudio2Voice.GetChannelVolumes
---

# IXAudio2Voice::GetChannelVolumes


## -description

Returns the volume levels for the voice, per channel.

## -parameters

### -param Channels [in]

Confirms the channel count of the voice.

### -param pVolumes [out]

Returns the current volume level of each channel in the voice. The array must have at least <i>Channels</i> elements. See Remarks for more information on volume levels.

## -returns

This method does not return a value.

## -remarks

These settings are applied after the effect chain is applied. This method is valid only for source and submix voices, because mastering voices do not specify volume per channel.



Volume levels are expressed as floating-point amplitude multipliers between -2²⁴ to 2²⁴, with a maximum gain of 144.5 dB. A volume of 1 means there is no attenuation or gain, 0 means silence, and negative levels can be used to invert the audio's phase. See <a href="/windows/desktop/xaudio2/xaudio2-volume-and-pitch-control">XAudio2 Volume and Pitch Control</a> for additional information on volume control.



<div class="alert"><b>Note</b>  <b>GetChannelVolumes</b> always returns the volume levels most recently set by <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes">IXAudio2Voice::SetChannelVolumes</a>. However, those values may not actually be in effect yet: they only take effect the next time the audio engine runs after the <b>IXAudio2Voice::SetChannelVolumes</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetChannelVolumes</b> was called with a deferred operation ID). </div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>