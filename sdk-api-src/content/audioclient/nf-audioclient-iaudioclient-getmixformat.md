---
UID: NF:audioclient.IAudioClient.GetMixFormat
title: IAudioClient::GetMixFormat (audioclient.h)
description: The GetMixFormat method retrieves the stream format that the audio engine uses for its internal processing of shared-mode streams.
helpviewer_keywords: ["GetMixFormat","GetMixFormat method [Core Audio]","GetMixFormat method [Core Audio]","IAudioClient interface","IAudioClient interface [Core Audio]","GetMixFormat method","IAudioClient.GetMixFormat","IAudioClient::GetMixFormat","IAudioClientGetMixFormat","audioclient/IAudioClient::GetMixFormat","coreaudio.iaudioclient_getmixformat"]
old-location: coreaudio\iaudioclient_getmixformat.htm
tech.root: CoreAudio
ms.assetid: 63f3e593-3904-44f9-a912-78c6c98e7597
ms.date: 12/05/2018
ms.keywords: GetMixFormat, GetMixFormat method [Core Audio], GetMixFormat method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetMixFormat method, IAudioClient.GetMixFormat, IAudioClient::GetMixFormat, IAudioClientGetMixFormat, audioclient/IAudioClient::GetMixFormat, coreaudio.iaudioclient_getmixformat
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
 - IAudioClient::GetMixFormat
 - audioclient/IAudioClient::GetMixFormat
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
 - IAudioClient.GetMixFormat
---

# IAudioClient::GetMixFormat


## -description

The <b>GetMixFormat</b> method retrieves the stream format that the audio engine uses for its internal processing of shared-mode streams.

## -parameters

### -param ppDeviceFormat [out]

Pointer to a pointer variable into which the method writes the address of the mix format. This parameter must be a valid, non-<b>NULL</b> pointer to a pointer variable. The method writes the address of a <b>WAVEFORMATEX</b> (or <b>WAVEFORMATEXTENSIBLE</b>) structure to this variable. The method allocates the storage for the structure. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetMixFormat</b> call fails, <i>*ppDeviceFormat</i> is <b>NULL</b>. For information about <b>WAVEFORMATEX</b>, <b>WAVEFORMATEXTENSIBLE</b>, and <b>CoTaskMemFree</b>, see the Windows SDK documentation.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppDeviceFormat</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

The client can call this method before calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method. When creating a shared-mode stream for an audio endpoint device, the <b>Initialize</b> method always accepts the stream format obtained from a <b>GetMixFormat</b> call on the same device.

The mix format is the format that the audio engine uses internally for digital processing of shared-mode streams. This format is not necessarily a format that the audio endpoint device supports. Thus, the caller might not succeed in creating an exclusive-mode stream with a format obtained by calling <b>GetMixFormat</b>.

For example, to facilitate digital audio processing, the audio engine might use a mix format that represents samples as floating-point values. If the device supports only integer PCM samples, then the engine converts the samples to or from integer PCM values at the connection between the device and the engine. However, to avoid resampling, the engine might use a mix format with a sample rate that the device supports.

To determine whether the <b>Initialize</b> method can create a shared-mode or exclusive-mode stream with a particular format, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-isformatsupported">IAudioClient::IsFormatSupported</a> method.

By itself, a <b>WAVEFORMATEX</b> structure cannot specify the mapping of channels to speaker positions. In addition, although <b>WAVEFORMATEX</b> specifies the size of the container for each audio sample, it cannot specify the number of bits of precision in a sample (for example, 20 bits of precision in a 24-bit container). However, the <b>WAVEFORMATEXTENSIBLE</b> structure can specify both the mapping of channels to speakers and the number of bits of precision in each sample. For this reason, the <b>GetMixFormat</b> method retrieves a format descriptor that is in the form of a <b>WAVEFORMATEXTENSIBLE</b> structure instead of a standalone <b>WAVEFORMATEX</b> structure. Through the <i>ppDeviceFormat</i> parameter, the method outputs a pointer to the <b>WAVEFORMATEX</b> structure that is embedded at the start of this <b>WAVEFORMATEXTENSIBLE</b> structure. For more information about <b>WAVEFORMATEX</b> and <b>WAVEFORMATEXTENSIBLE</b>, see the Windows DDK documentation.

For more information about the <b>GetMixFormat</b> method, see <a href="/windows/desktop/CoreAudio/device-formats">Device Formats</a>. For code examples that call <b>GetMixFormat</b>, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-isformatsupported">IAudioClient::IsFormatSupported</a>