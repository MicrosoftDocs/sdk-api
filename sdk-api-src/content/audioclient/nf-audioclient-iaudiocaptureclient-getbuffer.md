---
UID: NF:audioclient.IAudioCaptureClient.GetBuffer
title: IAudioCaptureClient::GetBuffer (audioclient.h)
description: Retrieves a pointer to the next available packet of data in the capture endpoint buffer.
helpviewer_keywords: ["GetBuffer","GetBuffer method [Core Audio]","GetBuffer method [Core Audio]","IAudioCaptureClient interface","IAudioCaptureClient interface [Core Audio]","GetBuffer method","IAudioCaptureClient.GetBuffer","IAudioCaptureClient::GetBuffer","IAudioCaptureClientGetBuffer","audioclient/IAudioCaptureClient::GetBuffer","coreaudio.iaudiocaptureclient_getbuffer"]
old-location: coreaudio\iaudiocaptureclient_getbuffer.htm
tech.root: CoreAudio
ms.assetid: 4298f584-39ce-4138-994a-0e551370429f
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [Core Audio], GetBuffer method [Core Audio],IAudioCaptureClient interface, IAudioCaptureClient interface [Core Audio],GetBuffer method, IAudioCaptureClient.GetBuffer, IAudioCaptureClient::GetBuffer, IAudioCaptureClientGetBuffer, audioclient/IAudioCaptureClient::GetBuffer, coreaudio.iaudiocaptureclient_getbuffer
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
 - IAudioCaptureClient::GetBuffer
 - audioclient/IAudioCaptureClient::GetBuffer
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
 - IAudioCaptureClient.GetBuffer
---

# IAudioCaptureClient::GetBuffer


## -description

Retrieves a pointer to the next available packet of data in the capture endpoint buffer.

## -parameters

### -param ppData [out]

Pointer to a pointer variable into which the method writes the starting address of the next data packet that is available for the client to read.

### -param pNumFramesToRead [out]

Pointer to a <b>UINT32</b> variable into which the method writes the frame count (the number of audio frames available in the data packet). The client should either read the entire data packet or none of it.

### -param pdwFlags [out]

Pointer to a <b>DWORD</b> variable into which the method writes the buffer-status flags. The method writes either 0 or the bitwise-OR combination of one or more of the following <a href="/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags">_AUDCLNT_BUFFERFLAGS</a> enumeration values:

AUDCLNT_BUFFERFLAGS_SILENT

AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY

AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR

<div class="alert"><b>Note</b>   The AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY flag is not supported in Windows Vista.<p class="note">In Windows 7 and later OS releases, this flag can be used for glitch detection. To start the capture stream, the client application must call <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a> followed by calls to <b>GetBuffer</b> in a loop to read data packets until all of the available packets in the endpoint buffer have been read. <b>GetBuffer</b> sets the AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY flag to indicate a glitch in the  buffer pointed by <i>ppData</i>.

</div>
<div> </div>

### -param pu64DevicePosition [out]

Pointer to a <b>UINT64</b> variable into which the method writes the device position of the first audio frame in the data packet. The device position is expressed as the number of audio frames from the start of the stream. This parameter can be <b>NULL</b> if the client does not require the device position. For more information, see Remarks.

### -param pu64QPCPosition [out]

Pointer to a <b>UINT64</b> variable into which the method writes the value of the performance counter at the time that the audio endpoint device recorded the device position of the first audio frame in the data packet. The method converts the counter value to 100-nanosecond units before writing it to <i>*pu64QPCPosition.</i> This parameter can be <b>NULL</b> if the client does not require the performance counter value. For more information, see Remarks.

## -returns

Possible return codes include, but are not limited to, the values shown in the following table.

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
The call succeeded and <i>*pNumFramesToRead</i> is nonzero, indicating that a packet is ready to be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_S_BUFFER_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and <i>*pNumFramesToRead</i> is 0, indicating that no capture data is available to be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_BUFFER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7 and later</b>: <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">GetBuffer</a> failed to retrieve a data buffer and *<i>ppData</i> points to <b>NULL</b>. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
A previous <b>IAudioCaptureClient::GetBuffer</b> call is still in effect.

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
<dt><b>AUDCLNT_E_BUFFER_OPERATION_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Buffer cannot be accessed because a stream reset is in progress.

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
Parameter ppData, pNumFramesToRead, or pdwFlags is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method retrieves the next data packet from the capture endpoint buffer. At a particular time, the buffer might contain zero, one, or more packets that are ready to read. Typically, a buffer-processing thread that reads data from a capture endpoint buffer reads all of the available packets each time the thread executes.

During processing of an audio capture stream, the client application alternately calls <b>GetBuffer</b> and the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer">IAudioCaptureClient::ReleaseBuffer</a> method. The client can read no more than a single data packet with each <b>GetBuffer</b> call. Following each <b>GetBuffer</b> call, the client must call <b>ReleaseBuffer</b> to release the packet before the client can call <b>GetBuffer</b> again to get the next packet.

Two or more consecutive calls either to <b>GetBuffer</b> or to <b>ReleaseBuffer</b> are not permitted and will fail with error code AUDCLNT_E_OUT_OF_ORDER. To ensure the correct ordering of calls, a <b>GetBuffer</b> call and its corresponding <b>ReleaseBuffer</b> call must occur in the same thread.

During each <b>GetBuffer</b> call, the caller must either obtain the entire packet or none of it. Before reading the packet, the caller can check the packet size (available through the <i>pNumFramesToRead</i> parameter) to make sure that it has enough room to store the entire packet.

During each <b>ReleaseBuffer</b> call, the caller reports the number of audio frames that it read from the buffer. This number must be either the (nonzero) packet size or 0. If the number is 0, then the next <b>GetBuffer</b> call will present the caller with the same packet as in the previous <b>GetBuffer</b> call.

Following each <b>GetBuffer</b> call, the data in the packet remains valid until the next <b>ReleaseBuffer</b> call releases the buffer.

The client must call <b>ReleaseBuffer</b> after a <b>GetBuffer</b> call that successfully obtains a packet of any size other than 0. The client has the option of calling or not calling <b>ReleaseBuffer</b> to release a packet of size 0.

The method outputs the device position and performance counter through the <i>pu64DevicePosition</i> and <i>pu64QPCPosition</i> output parameters. These values provide a time stamp for the first audio frame in the data packet. Through the <i>pdwFlags</i> output parameter, the method indicates whether the reported device position is valid.

The device position that the method writes to  <i>*pu64DevicePosition</i> is the stream-relative position of the audio frame that is currently playing through the speakers (for a rendering stream) or being recorded through the microphone (for a capture stream). The position is expressed as the number of frames from the start of the stream. The size of a frame in an audio stream is specified by the <b>nBlockAlign</b> member of the <b>WAVEFORMATEX</b> (or <b>WAVEFORMATEXTENSIBLE</b>) structure that specifies the stream format. The size, in bytes, of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, for a stereo (2-channel) stream with 16-bit samples, the frame size is four bytes.

The performance counter value that <b>GetBuffer</b> writes to <i>*pu64QPCPosition</i> is not the raw counter value obtained from the <b>QueryPerformanceCounter</b> function. If <i>t</i> is the raw counter value, and if <i>f</i> is the frequency obtained from the <b>QueryPerformanceFrequency</b> function, <b>GetBuffer</b> calculates the performance counter value as follows:

<i>*pu64QPCPosition</i> = 10,000,000<sup>.</sup><i>t</i>/<i>f</i>

The result is expressed in 100-nanosecond units. For more information about <b>QueryPerformanceCounter</b> and <b>QueryPerformanceFrequency</b>, see the Windows SDK documentation.

If no new packet is currently available, the method sets <i>*pNumFramesToRead</i> = 0 and returns status code AUDCLNT_S_BUFFER_EMPTY. In this case, the method does not write to the variables that are pointed to by the <i>ppData</i>, <i>pu64DevicePosition</i>, and <i>pu64QPCPosition</i> parameters.

Clients should avoid excessive delays between the <b>GetBuffer</b> call that acquires a packet and the <b>ReleaseBuffer</b> call that releases the packet. The implementation of the audio engine assumes that the <b>GetBuffer</b> call and the corresponding <b>ReleaseBuffer</b> call occur within the same buffer-processing period. Clients that delay releasing a packet for more than one period risk losing sample data.

In Windows 7 and later, <b>GetBuffer</b> can return the <b>AUDCLNT_E_BUFFER_ERROR</b> error code for an audio client that uses the endpoint buffer in the exclusive mode. This error indicates that the data buffer was not retrieved because a data packet wasn't available (*<i>ppData</i> received <b>NULL</b>).   

If <b>GetBuffer</b> returns <b>AUDCLNT_E_BUFFER_ERROR</b>, the thread consuming the audio samples must wait for the next processing pass. The client might benefit from keeping a count of the failed <b>GetBuffer</b> calls. If <b>GetBuffer</b> returns this error repeatedly, the client can start a new processing loop after shutting down the current client by calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">IAudioClient::Stop</a>, <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">IAudioClient::Reset</a>, and releasing the audio client.


#### Examples

For a code example that calls the <b>GetBuffer</b> method, see <a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiocaptureclient">IAudioCaptureClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer">IAudioCaptureClient::ReleaseBuffer</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getposition">IAudioClock::GetPosition</a>