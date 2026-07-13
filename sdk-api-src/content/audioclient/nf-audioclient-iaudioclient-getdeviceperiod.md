---
UID: NF:audioclient.IAudioClient.GetDevicePeriod
title: IAudioClient::GetDevicePeriod (audioclient.h)
description: The GetDevicePeriod method retrieves the length of the periodic interval separating successive processing passes by the audio engine on the data in the endpoint buffer.
helpviewer_keywords: ["GetDevicePeriod","GetDevicePeriod method [Core Audio]","GetDevicePeriod method [Core Audio]","IAudioClient interface","IAudioClient interface [Core Audio]","GetDevicePeriod method","IAudioClient.GetDevicePeriod","IAudioClient::GetDevicePeriod","IAudioClientGetDevicePeriod","audioclient/IAudioClient::GetDevicePeriod","coreaudio.iaudioclient_getdeviceperiod"]
old-location: coreaudio\iaudioclient_getdeviceperiod.htm
tech.root: CoreAudio
ms.assetid: f2f75fce-9eca-488d-b183-87d97d4e599a
ms.date: 12/05/2018
ms.keywords: GetDevicePeriod, GetDevicePeriod method [Core Audio], GetDevicePeriod method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetDevicePeriod method, IAudioClient.GetDevicePeriod, IAudioClient::GetDevicePeriod, IAudioClientGetDevicePeriod, audioclient/IAudioClient::GetDevicePeriod, coreaudio.iaudioclient_getdeviceperiod
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
 - IAudioClient::GetDevicePeriod
 - audioclient/IAudioClient::GetDevicePeriod
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
 - IAudioClient.GetDevicePeriod
---

# IAudioClient::GetDevicePeriod


## -description

The <b>GetDevicePeriod</b> method retrieves the length of the periodic interval separating successive processing passes by the audio engine on the data in the endpoint buffer.

## -parameters

### -param phnsDefaultDevicePeriod [out]

Pointer to a <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> variable into which the method writes a time value specifying the default interval between periodic processing passes by the audio engine. The time is expressed in 100-nanosecond units. For information about <b>REFERENCE_TIME</b>, see the Windows SDK documentation.

### -param phnsMinimumDevicePeriod [out]

Pointer to a <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> variable into which the method writes a time value specifying the minimum interval between periodic processing passes by the audio endpoint device. The time is expressed in 100-nanosecond units.

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
Parameters <i>phnsDefaultDevicePeriod</i> and <i>phnsMinimumDevicePeriod</i> are both <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The client can call this method before calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

The <i>phnsDefaultDevicePeriod</i> parameter specifies the default scheduling period for a shared-mode stream. The <i>phnsMinimumDevicePeriod</i> parameter specifies the minimum scheduling period for an exclusive-mode stream.

At least one of the two parameters, <i>phnsDefaultDevicePeriod</i> and <i>phnsMinimumDevicePeriod</i>, must be non-<b>NULL</b> or the method returns immediately with error code E_POINTER. If both parameters are non-<b>NULL</b>, then the method outputs both the default and minimum periods.

For a shared-mode stream, the audio engine periodically processes the data in the endpoint buffer, which the engine shares with the client application. The engine schedules itself to perform these processing passes at regular intervals.

The period between processing passes by the audio engine is fixed for a particular audio endpoint device and represents the smallest processing quantum for the audio engine. This period plus the stream latency between the buffer and endpoint device represents the minimum possible latency that an audio application can achieve.

The client has the option of scheduling its periodic processing thread to run at the same time interval as the audio engine. In this way, the client can achieve the smallest possible latency for a shared-mode stream. However, in an application for which latency is less important, the client can reduce the process-switching overhead on the CPU by scheduling its processing passes to occur less frequently. In this case, the endpoint buffer must be proportionally larger to compensate for the longer period between processing passes.

The client determines the buffer size during its call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method. For a shared-mode stream, if the client passes this method an <i>hnsBufferDuration</i> parameter value of 0, the method assumes that the periods for the client and audio engine are guaranteed to be equal, and the method will allocate a buffer small enough to achieve the minimum possible latency. (In fact, any <i>hnsBufferDuration</i> value between 0 and the sum of the audio engine's period and device latency will have the same result.) Similarly, for an exclusive-mode stream, if the client sets <i>hnsBufferDuration</i> to 0, the method assumes that the period of the client is set to the minimum period of the audio endpoint device, and the method will allocate a buffer small enough to achieve the minimum possible latency.

If the client chooses to run its periodic processing thread less often, at the cost of increased latency, it can do so as long as it creates an endpoint buffer during the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> call that is sufficiently large.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>