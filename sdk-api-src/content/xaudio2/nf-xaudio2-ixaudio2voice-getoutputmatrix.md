---
UID: NF:xaudio2.IXAudio2Voice.GetOutputMatrix
title: IXAudio2Voice::GetOutputMatrix (xaudio2.h)
description: Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.
helpviewer_keywords: ["GetOutputMatrix","GetOutputMatrix method [XAudio2 Audio Mixing APIs]","GetOutputMatrix method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","GetOutputMatrix method","IXAudio2Voice.GetOutputMatrix","IXAudio2Voice::GetOutputMatrix","xaudio2.ixaudio2voice_interface_getoutputmatrix","xaudio2/IXAudio2Voice::GetOutputMatrix"]
old-location: xaudio2\ixaudio2voice_interface_getoutputmatrix.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetOutputMatrix(IXAudio2Voice,UINT32,UINT32,float@)
ms.date: 12/05/2018
ms.keywords: GetOutputMatrix, GetOutputMatrix method [XAudio2 Audio Mixing APIs], GetOutputMatrix method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetOutputMatrix method, IXAudio2Voice.GetOutputMatrix, IXAudio2Voice::GetOutputMatrix, xaudio2.ixaudio2voice_interface_getoutputmatrix, xaudio2/IXAudio2Voice::GetOutputMatrix
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
 - IXAudio2Voice::GetOutputMatrix
 - xaudio2/IXAudio2Voice::GetOutputMatrix
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
 - IXAudio2Voice.GetOutputMatrix
---

# IXAudio2Voice::GetOutputMatrix


## -description

Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

## -parameters

### -param pDestinationVoice [in]

Pointer specifying the destination <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a> to retrieve the output matrix for.

<div class="alert"><b>Note</b>  If the voice sends to a single target voice then specifying NULL will cause <b>GetOutputMatrix</b> to operate on that target voice.</div>
<div> </div>

### -param SourceChannels [in]

Confirms the output channel count of the voice. This is the number of channels that are produced by the last effect in the chain.

### -param DestinationChannels [in]

Confirms the input channel count of the destination voice.

### -param pLevelMatrix [out]

Array of [<i>SourceChannels</i> * <i>DestinationChannels</i>] volume levels sent to the destination voice. The level sent from source channel S to destination channel D is returned in the form <i>pLevelMatrix</i>[<i>DestinationChannels</i> × S + D]. See Remarks for more information on volume levels.

## -returns

This method does not return a value.

## -remarks

This method applies only to source and submix voices, because mastering voices write directly to the device with no matrix mixing.

Volume levels are expressed as floating-point amplitude multipliers between -2²⁴ to 2²⁴, with a maximum gain of 144.5 dB. A volume level of 1 means there is no attenuation or gain and 0 means silence. Negative levels can be used to invert the audio's phase. See <a href="/windows/desktop/xaudio2/xaudio2-volume-and-pitch-control">XAudio2 Volume and Pitch Control</a> for additional information on volume control.



See <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a> for information on standard channel ordering.



<div class="alert"><b>Note</b>  <b>GetOutputMatrix</b> always returns the levels most recently set by <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix">IXAudio2Voice::SetOutputMatrix</a>. However, they may not actually be in effect yet: they only take effect the next time the audio engine runs after the <b>IXAudio2Voice::SetOutputMatrix</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetOutputMatrix</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>