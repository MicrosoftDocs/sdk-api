---
UID: NF:audioclient.IAudioClient3.InitializeSharedAudioStream
title: IAudioClient3::InitializeSharedAudioStream (audioclient.h)
description: Initializes a shared stream with the specified periodicity.
helpviewer_keywords: ["IAudioClient3 interface [Core Audio]","InitializeSharedAudioStream method","IAudioClient3.InitializeSharedAudioStream","IAudioClient3::InitializeSharedAudioStream","InitializeSharedAudioStream","InitializeSharedAudioStream method [Core Audio]","InitializeSharedAudioStream method [Core Audio]","IAudioClient3 interface","audioclient/IAudioClient3::InitializeSharedAudioStream","coreaudio.iaudioclient3_initializesharedaudiostream"]
old-location: coreaudio\iaudioclient3_initializesharedaudiostream.htm
tech.root: CoreAudio
ms.assetid: 2DB9ECEC-8199-4157-8854-26A21B88E58A
ms.date: 12/05/2018
ms.keywords: IAudioClient3 interface [Core Audio],InitializeSharedAudioStream method, IAudioClient3.InitializeSharedAudioStream, IAudioClient3::InitializeSharedAudioStream, InitializeSharedAudioStream, InitializeSharedAudioStream method [Core Audio], InitializeSharedAudioStream method [Core Audio],IAudioClient3 interface, audioclient/IAudioClient3::InitializeSharedAudioStream, coreaudio.iaudioclient3_initializesharedaudiostream
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IAudioClient3::InitializeSharedAudioStream
 - audioclient/IAudioClient3::InitializeSharedAudioStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClient3.InitializeSharedAudioStream
---

# IAudioClient3::InitializeSharedAudioStream


## -description

Initializes a shared stream with the specified periodicity.

## -parameters

### -param StreamFlags [in]

Type: <b>DWORD</b>

Flags to control creation of the stream. The client should set this parameter to 0 or to the bitwise OR of one or more of the supported  <a href="/windows/desktop/CoreAudio/audclnt-streamflags-xxx-constants">AUDCLNT_STREAMFLAGS_XXX Constants</a> or   <a href="/windows/desktop/CoreAudio/audclnt-sessionflags-xxx-constants">AUDCLNT_SESSIONFLAGS_XXX Constants</a>. The supported <a href="/windows/desktop/CoreAudio/audclnt-streamflags-xxx-constants">AUDCLNT_STREAMFLAGS_XXX Constants</a> for this parameter when using this method are: 

- AUDCLNT_STREAMFLAGS_EVENTCALLBACK

### -param PeriodInFrames [in]

Type: <b>UINT32</b>

Periodicity requested by the client. This value must  be an integral multiple of the value returned in the <i>pFundamentalPeriodInFrames</i> parameter to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-getsharedmodeengineperiod">IAudioClient3::GetSharedModeEnginePeriod</a>.  <i>PeriodInFrames</i> must also be greater than or equal to the value returned in <i>pMinPeriodInFrames</i> and less than or equal to the value returned in <i>pMaxPeriodInFrames</i>.

### -param pFormat [in]

Type: <b>const <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>*</b>

Pointer to a format descriptor. This parameter must point to a valid format descriptor of type <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> or <b></b><a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>. For more information, see the Remarks section for <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>.

### -param AudioSessionGuid [in, optional]

Type: <b>LPCGUID</b>

Pointer to a session GUID. This parameter points to a GUID value that identifies the audio session that the stream belongs to. If the GUID identifies a session that has been previously opened, the method adds the stream to that session. If the GUID does not identify an existing session, the method opens a new session and adds the stream to that session. The stream remains a member of the same session for its lifetime. Setting this parameter to <b>NULL</b> is equivalent to passing a pointer to a GUID_NULL value.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <b>IAudioClient</b> object is already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_WRONG_ENDPOINT_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The AUDCLNT_STREAMFLAGS_LOOPBACK flag is set but the endpoint device is a capture device, not a rendering device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_CPUUSAGE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the process-pass duration exceeded the maximum CPU usage. The audio engine keeps track of CPU usage by maintaining the number of times the process-pass duration exceeds the maximum CPU usage. The maximum CPU usage is calculated as a percent of  the engine's periodicity. The percentage value is the system's CPU throttle value (within the range of 10% and 90%). If  this value is not found, then the default value of 40% is used to calculate the maximum CPU usage. 



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
<dt><b>AUDCLNT_E_DEVICE_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The endpoint device is already in use. Either the device is being used in exclusive mode, or the device is being used in shared mode and the caller asked to use the device in exclusive mode.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_ENGINE_FORMAT_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The client specified <a href="/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions">AUDCLNT_STREAMOPTIONS_MATCH_FORMAT</a> when calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">IAudioClient2::SetClientProperties</a>, but the format of the audio engine has been locked by another client. In this case, you can call <b>IAudioClient2::SetClientProperties</b> without specifying the match format option and then use audio engine's current format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_ENGINE_PERIODICITY_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The client specified <a href="/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions">AUDCLNT_STREAMOPTIONS_MATCH_FORMAT</a> when calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">IAudioClient2::SetClientProperties</a>, but the periodicity of the audio engine has been locked by another client. In this case, you can call <b>IAudioClient2::SetClientProperties</b> without specifying the match format option and then use audio engine's current periodicity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_ENDPOINT_CREATE_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The method failed to create the audio endpoint for the render or the capture device. This can occur if the audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_INVALID_DEVICE_PERIOD</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the requested device period specified with the <i>PeriodInFrames</i> is not an integral multiple of the fundamental periodicity of the audio engine, is shorter than the engine's minimum period, or is longer than the engine's maximum period. Get the supported periodicity values of the engine by calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-getsharedmodeengineperiod">IAudioClient3::GetSharedModeEnginePeriod</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_UNSUPPORTED_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The audio engine (shared mode) or audio endpoint device (exclusive mode) does not support the specified format.

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
Parameter <i>pFormat</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pFormat</i> points to an invalid format description; or the AUDCLNT_STREAMFLAGS_LOOPBACK flag is set but <i>ShareMode</i> is not equal to AUDCLNT_SHAREMODE_SHARED; or the AUDCLNT_STREAMFLAGS_CROSSPROCESS flag is set but <i>ShareMode</i> is equal to AUDCLNT_SHAREMODE_EXCLUSIVE.

A prior call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">SetClientProperties</a> was made with an invalid category for audio/render streams.

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
</table>

## -remarks

Unlike <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>, this method does not allow you to specify a  buffer size. The buffer size is computed based on the periodicity requested with the <i>PeriodInFrames</i> parameter. It is the client app's responsibility
    to ensure that audio samples are transferred in and out of the buffer in a timely manner. 

Audio clients should check for allowed values for the <i>PeriodInFrames</i> parameter by calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-getsharedmodeengineperiod">IAudioClient3::GetSharedModeEnginePeriod</a>. The value of <i>PeriodInFrames</i> must be an integral multiple of the value returned in the <i>pFundamentalPeriodInFrames</i> parameter.  <i>PeriodInFrames</i> must also be greater than or equal to the value returned in <i>pMinPeriodInFrames</i> and less than or equal to the value of <i>pMaxPeriodInFrames</i>.

For example, for a 44100 kHz format, <b>GetSharedModeEnginePeriod</b> might return:

* <i>pDefaultPeriodInFrames</i> = 448 frames (about 10.16 milliseconds)

* <i>pFundamentalPeriodInFrames</i> = 4 frames (about 0.09 milliseconds)

* <i>pMinPeriodInFrames</i> = 48 frames (about 1.09 milliseconds)

* <i>pMaxPeriodInFrames</i> = 448 frames (same as the default)

Allowed values for the <i>PeriodInFrames</i> parameter to <b>InitializeSharedAudioStream</b> would include 48 and 448. They would also include things like 96 and 128.

They would NOT include 4 (which is smaller than the minimum allowed value) or 98 (which is not a multiple of the fundamental) or 1000 (which is larger than the maximum allowed value).

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2">IAudioClient2</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient3">IAudioClient3</a>