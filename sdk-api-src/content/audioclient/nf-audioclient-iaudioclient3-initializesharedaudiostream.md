---
UID: NF:audioclient.IAudioClient3.InitializeSharedAudioStream
title: IAudioClient3::InitializeSharedAudioStream
author: windows-sdk-content
description: Initializes a shared stream with the specified periodicity.
old-location: coreaudio\iaudioclient3_initializesharedaudiostream.htm
old-project: CoreAudio
ms.assetid: 2DB9ECEC-8199-4157-8854-26A21B88E58A
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IAudioClient3 interface [Core Audio],InitializeSharedAudioStream method, IAudioClient3.InitializeSharedAudioStream, IAudioClient3::InitializeSharedAudioStream, InitializeSharedAudioStream, InitializeSharedAudioStream method [Core Audio], InitializeSharedAudioStream method [Core Audio],IAudioClient3 interface, audioclient/IAudioClient3::InitializeSharedAudioStream, coreaudio.iaudioclient3_initializesharedaudiostream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClient3.InitializeSharedAudioStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient3::InitializeSharedAudioStream


## -description


Initializes a shared stream with the specified periodicity.


## -parameters




### -param StreamFlags [in]

Type: <b>DWORD</b>

Flags to control creation of the stream. The client should set this parameter to 0 or to the bitwise OR of one or more of the supported  <a href="https://msdn.microsoft.com/7b2267c3-79f5-4ada-a7ce-78dd514f8487">AUDCLNT_STREAMFLAGS_XXX Constants</a> or   <a href="https://msdn.microsoft.com/5745d5bc-71e8-4b33-8227-c1c84226b6ee">AUDCLNT_SESSIONFLAGS_XXX Constants</a>. The supported constants for this parameter are: 


### -param PeriodInFrames [in]

Type: <b>UINT32</b>

Periodicity requested by the client. This value must  be an integral multiple of the value returned in the <i>pDefaultPeriodInFrames</i> parameter to <a href="https://msdn.microsoft.com/41ED045F-0C47-40BE-9ECD-6A925E166E6D">IAudioClient3::GetSharedModeEnginePeriod</a>.  <i>PeriodInFrames</i> must also be greater than or equal to the value returned in <i>pMinPeriodInFrames</i> and less than or equal to the value of returned<i>pMaxPeriodInFrames</i>.


### -param pFormat [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>*</b>

Pointer to a format descriptor. This parameter must point to a valid format descriptor of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> or <b></b><a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a>. For more information, see the Remarks section for <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>.


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
The client specified <a href="https://msdn.microsoft.com/C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7">AUDCLNT_STREAMOPTIONS_MATCH_FORMAT</a> when calling <a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">IAudioClient2::SetClientProperties</a>, but the format of the audio engine has been locked by another client. In this case, you can call <b>IAudioClient2::SetClientProperties</b> without specifying the match format option and then use audio engine's current format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_ENGINE_PERIODICITY_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The client specified <a href="https://msdn.microsoft.com/C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7">AUDCLNT_STREAMOPTIONS_MATCH_FORMAT</a> when calling <a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">IAudioClient2::SetClientProperties</a>, but the periodicity of the audio engine has been locked by another client. In this case, you can call <b>IAudioClient2::SetClientProperties</b> without specifying the match format option and then use audio engine's current periodicity.

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
Indicates that the requested device period specified with the <i>PeriodInFrames</i> is not an integral multiple of the fundamental periodicity of the audio engine, is shorter than the engine's minimum period, or is longer than the engine's maximum period. Get the supported periodicity values of the engine by calling <a href="https://msdn.microsoft.com/41ED045F-0C47-40BE-9ECD-6A925E166E6D">IAudioClient3::GetSharedModeEnginePeriod</a>.

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

A prior call to <a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">SetClientProperties</a> was made with an invalid category for audio/render streams.

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



Unlike <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>, this method does not allow you to specify a  buffer size. The buffer size is computed based on the periodicity requested with the <i>PeriodInFrames</i> parameter. It is the client app's responsibility
    to ensure that audio samples are transferred in and out of the buffer in a timely manner. 




## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a>



<a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>



<a href="https://msdn.microsoft.com/E8EFE682-E1BC-4D0D-A60E-DD257D6E5894">IAudioClient3</a>
 

 

