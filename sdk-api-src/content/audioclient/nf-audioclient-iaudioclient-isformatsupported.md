---
UID: NF:audioclient.IAudioClient.IsFormatSupported
title: IAudioClient::IsFormatSupported (audioclient.h)
description: The IsFormatSupported method indicates whether the audio endpoint device supports a particular stream format.
helpviewer_keywords: ["IAudioClient interface [Core Audio]","IsFormatSupported method","IAudioClient.IsFormatSupported","IAudioClient::IsFormatSupported","IAudioClientIsFormatSupported","IsFormatSupported","IsFormatSupported method [Core Audio]","IsFormatSupported method [Core Audio]","IAudioClient interface","audioclient/IAudioClient::IsFormatSupported","coreaudio.iaudioclient_isformatsupported"]
old-location: coreaudio\iaudioclient_isformatsupported.htm
tech.root: CoreAudio
ms.assetid: 92d1fc93-08e2-46d9-bd2f-ce1b2087d2d1
ms.date: 12/05/2018
ms.keywords: IAudioClient interface [Core Audio],IsFormatSupported method, IAudioClient.IsFormatSupported, IAudioClient::IsFormatSupported, IAudioClientIsFormatSupported, IsFormatSupported, IsFormatSupported method [Core Audio], IsFormatSupported method [Core Audio],IAudioClient interface, audioclient/IAudioClient::IsFormatSupported, coreaudio.iaudioclient_isformatsupported
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioClient::IsFormatSupported
 - audioclient/IAudioClient::IsFormatSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient.IsFormatSupported
---

# IAudioClient::IsFormatSupported


## -description

The <b>IsFormatSupported</b> method indicates whether the audio endpoint device supports a particular stream format.

## -parameters

### -param ShareMode [in]

The sharing mode for the stream format. Through this parameter, the client indicates whether it wants to use the specified format in exclusive mode or shared mode. The client should set this parameter to one of the following <a href="/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode">AUDCLNT_SHAREMODE</a> enumeration values:

AUDCLNT_SHAREMODE_EXCLUSIVE

AUDCLNT_SHAREMODE_SHARED

### -param pFormat [in]

Pointer to the specified stream format. This parameter points to a caller-allocated format descriptor of type <b>WAVEFORMATEX</b> or <b>WAVEFORMATEXTENSIBLE</b>. The client writes a format description to this structure before calling this method. For information about <b>WAVEFORMATEX</b> and <b>WAVEFORMATEXTENSIBLE</b>, see the Windows DDK documentation.

### -param ppClosestMatch [out]

Pointer to a pointer variable into which the method writes the address of a <b>WAVEFORMATEX</b> or <b>WAVEFORMATEXTENSIBLE</b> structure. This structure specifies the supported format that is closest to the format that the client specified through the <i>pFormat</i> parameter. For shared mode (that is, if the <i>ShareMode</i> parameter is AUDCLNT_SHAREMODE_SHARED), set <i>ppClosestMatch</i> to point to a valid, non-<b>NULL</b> pointer variable. For exclusive mode, set <i>ppClosestMatch</i> to <b>NULL</b>. The method allocates the storage for the structure. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>IsFormatSupported</b> call fails and <i>ppClosestMatch</i> is non-<b>NULL</b>, the method sets <i>*ppClosestMatch</i> to <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Succeeded and the audio endpoint device supports the specified stream format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Succeeded with  a closest match to the specified format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_UNSUPPORTED_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Succeeded but the specified format is not supported in exclusive mode.

</td>
</tr>
</table>
 

 If the operation fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pFormat</i> is <b>NULL</b>, or <i>ppClosestMatch</i> is <b>NULL</b> and <i>ShareMode</i> is AUDCLNT_SHAREMODE_SHARED.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ShareMode</i> is a value other than AUDCLNT_SHAREMODE_SHARED or AUDCLNT_SHAREMODE_EXCLUSIVE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The stream's resources have been invalidated. This error may be thrown for the following reasons:<br>
- The stream is suspended.<br>
- An Exclusive or Offload stream is disconnected.<br>
- A packaged application that has an exclusive mode or offload stream is quiesced.<br>
- A "protected output" stream is closed.<br>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>

## -remarks

This method provides a way for a client to determine, before calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>, whether the audio engine supports a particular stream format.

For exclusive mode, <b>IsFormatSupported</b> returns S_OK if the audio endpoint device supports the caller-specified format, or it returns AUDCLNT_E_UNSUPPORTED_FORMAT if the device does not support the format. The <i>ppClosestMatch</i> parameter can be <b>NULL</b>. If it is not <b>NULL</b>, the method writes <b>NULL</b> to <i>*ppClosestMatch</i>.

For shared mode, if the audio engine supports the caller-specified format, <b>IsFormatSupported</b> sets <b>*ppClosestMatch</b> to <b>NULL</b> and returns S_OK. If the audio engine does not support the caller-specified format but does support a similar format, the method retrieves the similar format through the <i>ppClosestMatch</i> parameter and returns S_FALSE. If the audio engine does not support the caller-specified format or any similar format, the method sets  <i>*ppClosestMatch</i> to <b>NULL</b> and returns AUDCLNT_E_UNSUPPORTED_FORMAT.

In shared mode, the audio engine always supports the mix format, which the client can obtain by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a> method. In addition, the audio engine might support similar formats that have the same sample rate and number of channels as the mix format but differ in the representation of audio sample values. The audio engine represents sample values internally as floating-point numbers, but if the caller-specified format represents sample values as integers, the audio engine typically can convert between the integer sample values and its internal floating-point representation.

The audio engine might be able to support an even wider range of shared-mode formats if the installation package for the audio device includes a local effects (LFX) audio processing object (APO) that can handle format conversions. An LFX APO is a software module that performs device-specific processing of an audio stream. The audio graph builder in the Windows audio service inserts the LFX APO into the stream between each client and the audio engine. When a client calls the <b>IsFormatSupported</b> method and the method determines that an LFX APO is installed for use with the device, the method directs the query to the LFX APO, which indicates whether it supports the caller-specified format.

For example, a particular LFX APO might accept a 6-channel surround sound stream from a client and convert the stream to a stereo format that can be played through headphones. Typically, an LFX APO supports only client formats with sample rates that match the sample rate of the mix format.

For more information about APOs, see [Windows Audio Processing Objects](/windows-hardware/drivers/audio/windows-audio-processing-objects). For more information about the <b>IsFormatSupported</b> method, see <a href="/windows/desktop/CoreAudio/device-formats">Device Formats</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>