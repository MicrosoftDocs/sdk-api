---
UID: NF:audioclient.IAudioCaptureClient.GetNextPacketSize
title: IAudioCaptureClient::GetNextPacketSize (audioclient.h)
description: The GetNextPacketSize method retrieves the number of frames in the next data packet in the capture endpoint buffer.
helpviewer_keywords: ["GetNextPacketSize","GetNextPacketSize method [Core Audio]","GetNextPacketSize method [Core Audio]","IAudioCaptureClient interface","IAudioCaptureClient interface [Core Audio]","GetNextPacketSize method","IAudioCaptureClient.GetNextPacketSize","IAudioCaptureClient::GetNextPacketSize","IAudioCaptureClientGetNextPacketSize","audioclient/IAudioCaptureClient::GetNextPacketSize","coreaudio.iaudiocaptureclient_getnextpacketsize"]
old-location: coreaudio\iaudiocaptureclient_getnextpacketsize.htm
tech.root: CoreAudio
ms.assetid: 352dcd7d-a7e1-493f-b9ce-c125f9d45fa8
ms.date: 12/05/2018
ms.keywords: GetNextPacketSize, GetNextPacketSize method [Core Audio], GetNextPacketSize method [Core Audio],IAudioCaptureClient interface, IAudioCaptureClient interface [Core Audio],GetNextPacketSize method, IAudioCaptureClient.GetNextPacketSize, IAudioCaptureClient::GetNextPacketSize, IAudioCaptureClientGetNextPacketSize, audioclient/IAudioCaptureClient::GetNextPacketSize, coreaudio.iaudiocaptureclient_getnextpacketsize
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
 - IAudioCaptureClient::GetNextPacketSize
 - audioclient/IAudioCaptureClient::GetNextPacketSize
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
 - IAudioCaptureClient.GetNextPacketSize
---

# IAudioCaptureClient::GetNextPacketSize


## -description

The <b>GetNextPacketSize</b> method retrieves the number of frames in the next data packet in the capture endpoint buffer.

## -parameters

### -param pNumFramesInNextPacket [out]

Pointer to a <b>UINT32</b> variable into which the method writes the frame count (the number of audio frames in the next capture packet).

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
Parameter <i>pNumFramesInNextPacket</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Use this method only with shared-mode streams. It does not work with exclusive-mode streams.

Before calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a> method to retrieve the next data packet, the client can call <b>GetNextPacketSize</b> to retrieve the number of audio frames in the next packet. The count reported by <b>GetNextPacketSize</b> matches the count retrieved in the <b>GetBuffer</b> call (through the <i>pNumFramesToRead</i> output parameter) that follows the <b>GetNextPacketSize</b> call.

A packet always consists of an integral number of audio frames.

<b>GetNextPacketSize</b> must be called in the same thread as the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">GetBuffer</a> and <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer">IAudioCaptureClient::ReleaseBuffer</a> method calls that get and release the packets in the capture endpoint buffer.

For a code example that uses the <b>GetNextPacketSize</b> method, see <a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiocaptureclient">IAudioCaptureClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer">IAudioCaptureClient::ReleaseBuffer</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getcurrentpadding">IAudioClient::GetCurrentPadding</a>