---
UID: NF:audioclient.IAudioCaptureClient.ReleaseBuffer
title: IAudioCaptureClient::ReleaseBuffer (audioclient.h)
description: The ReleaseBuffer method releases the buffer.
helpviewer_keywords: ["IAudioCaptureClient interface [Core Audio]","ReleaseBuffer method","IAudioCaptureClient.ReleaseBuffer","IAudioCaptureClient::ReleaseBuffer","IAudioCaptureClientReleaseBuffer","ReleaseBuffer","ReleaseBuffer method [Core Audio]","ReleaseBuffer method [Core Audio]","IAudioCaptureClient interface","audioclient/IAudioCaptureClient::ReleaseBuffer","coreaudio.iaudiocaptureclient_releasebuffer"]
old-location: coreaudio\iaudiocaptureclient_releasebuffer.htm
tech.root: CoreAudio
ms.assetid: 38e1ea6c-d07d-4075-b6f2-d563c4bce007
ms.date: 12/05/2018
ms.keywords: IAudioCaptureClient interface [Core Audio],ReleaseBuffer method, IAudioCaptureClient.ReleaseBuffer, IAudioCaptureClient::ReleaseBuffer, IAudioCaptureClientReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [Core Audio], ReleaseBuffer method [Core Audio],IAudioCaptureClient interface, audioclient/IAudioCaptureClient::ReleaseBuffer, coreaudio.iaudiocaptureclient_releasebuffer
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
 - IAudioCaptureClient::ReleaseBuffer
 - audioclient/IAudioCaptureClient::ReleaseBuffer
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
 - IAudioCaptureClient.ReleaseBuffer
---

# IAudioCaptureClient::ReleaseBuffer


## -description

The <b>ReleaseBuffer</b> method releases the buffer.

## -parameters

### -param NumFramesRead [in]

The number of audio frames that the client read from the capture buffer. This parameter must be either equal to the number of frames in the previously acquired data packet or 0.

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
<dt><b>AUDCLNT_E_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>NumFramesRead</i> parameter is set to a value other than the data packet size or 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
This call was not preceded by a corresponding <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a> call.

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

The client should call this method when it finishes reading a data packet that it obtained previously by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a> method.

The data in the packet that the client obtained from a <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">GetBuffer</a> call is guaranteed to remain valid until the client calls <b>ReleaseBuffer</b> to release the packet.

Between each <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">GetBuffer</a> call and its corresponding <b>ReleaseBuffer</b> call, the client must either read the entire data packet or none of it. If the client reads the entire packet following the <b>GetBuffer</b> call, then it should call <b>ReleaseBuffer</b> with <i>NumFramesRead</i> set to the total number of frames in the data packet. In this case, the next call to <b>GetBuffer</b> will produce a new data packet. If the client reads none of the data from the packet following the call to <b>GetBuffer</b>, then it should call <b>ReleaseBuffer</b> with <i>NumFramesRead</i> set to 0. In this case, the next <b>GetBuffer</b> call will produce the same data packet as in the previous <b>GetBuffer</b> call.

If the client calls <b>ReleaseBuffer</b> with <i>NumFramesRead</i> set to any value other than the packet size or 0, then the call fails and returns error code AUDCLNT_E_INVALID_SIZE.

Clients should avoid excessive delays between the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">GetBuffer</a> call that acquires a buffer and the <b>ReleaseBuffer</b> call that releases the buffer. The implementation of the audio engine assumes that the <b>GetBuffer</b> call and the corresponding <b>ReleaseBuffer</b> call occur within the same buffer-processing period. Clients that delay releasing a buffer for more than one period risk losing sample data.

For a code example that calls the <b>ReleaseBuffer</b> method, see <a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiocaptureclient">IAudioCaptureClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a>