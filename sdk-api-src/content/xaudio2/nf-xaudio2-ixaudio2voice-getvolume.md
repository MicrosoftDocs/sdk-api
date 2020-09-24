---
UID: NF:xaudio2.IXAudio2Voice.GetVolume
title: IXAudio2Voice::GetVolume (xaudio2.h)
description: Gets the current overall volume level of the voice.
helpviewer_keywords: ["GetVolume","GetVolume method [XAudio2 Audio Mixing APIs]","GetVolume method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","GetVolume method","IXAudio2Voice.GetVolume","IXAudio2Voice::GetVolume","xaudio2.ixaudio2voice_interface_getvolume","xaudio2/IXAudio2Voice::GetVolume"]
old-location: xaudio2\ixaudio2voice_interface_getvolume.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetVolume(float@)
ms.date: 12/05/2018
ms.keywords: GetVolume, GetVolume method [XAudio2 Audio Mixing APIs], GetVolume method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetVolume method, IXAudio2Voice.GetVolume, IXAudio2Voice::GetVolume, xaudio2.ixaudio2voice_interface_getvolume, xaudio2/IXAudio2Voice::GetVolume
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
 - IXAudio2Voice::GetVolume
 - xaudio2/IXAudio2Voice::GetVolume
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
 - IXAudio2Voice.GetVolume
---

# IXAudio2Voice::GetVolume


## -description

Gets the current overall volume level of the voice.

## -parameters

### -param pVolume [out]

Returns the current overall volume level of the voice. See Remarks for more information on volume levels.

## -returns

This method does not return a value.

## -remarks

Volume levels are expressed as floating-point amplitude multipliers between -224 to 224, with a maximum gain of 144.5 dB. A volume level of 1 means there is no attenuation or gain and 0 means silence. Negative levels can be used to invert the audio's phase. See <a href="/windows/desktop/xaudio2/xaudio2-volume-and-pitch-control">XAudio2 Volume and Pitch Control</a> for additional information on volume control.



<div class="alert"><b>Note</b>  <b>GetVolume</b> always returns the volume most recently set by <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume">IXAudio2Voice::SetVolume</a>. However, it may not actually be in effect yet: it only takes effect the next time the audio engine runs after the <b>IXAudio2Voice::SetVolume</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetVolume</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>