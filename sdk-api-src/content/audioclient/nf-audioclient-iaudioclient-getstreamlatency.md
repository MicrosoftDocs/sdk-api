---
UID: NF:audioclient.IAudioClient.GetStreamLatency
title: IAudioClient::GetStreamLatency (audioclient.h)
description: The GetStreamLatency method retrieves the maximum latency for the current stream and can be called any time after the stream has been initialized.
helpviewer_keywords: ["GetStreamLatency","GetStreamLatency method [Core Audio]","GetStreamLatency method [Core Audio]","IAudioClient interface","IAudioClient interface [Core Audio]","GetStreamLatency method","IAudioClient.GetStreamLatency","IAudioClient::GetStreamLatency","IAudioClientGetStreamLatency","audioclient/IAudioClient::GetStreamLatency","coreaudio.iaudioclient_getstreamlatency"]
old-location: coreaudio\iaudioclient_getstreamlatency.htm
tech.root: CoreAudio
ms.assetid: ccc06e31-e56f-4910-882a-40b1ce0b43aa
ms.date: 12/05/2018
ms.keywords: GetStreamLatency, GetStreamLatency method [Core Audio], GetStreamLatency method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetStreamLatency method, IAudioClient.GetStreamLatency, IAudioClient::GetStreamLatency, IAudioClientGetStreamLatency, audioclient/IAudioClient::GetStreamLatency, coreaudio.iaudioclient_getstreamlatency
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
 - IAudioClient::GetStreamLatency
 - audioclient/IAudioClient::GetStreamLatency
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
 - IAudioClient.GetStreamLatency
---

# IAudioClient::GetStreamLatency


## -description

The <b>GetStreamLatency</b> method retrieves the maximum latency for the current stream and can be called any time after the stream has been initialized.

## -parameters

### -param phnsLatency [out]

Pointer to a <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> variable into which the method writes a time value representing the latency. The time is expressed in 100-nanosecond units. For more information about <b>REFERENCE_TIME</b>, see the Windows SDK documentation.

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
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been successfully initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
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
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

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
Parameter <i>phnsLatency</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

This method retrieves the maximum latency for the current stream. The value will not change for the lifetime of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> object.

Rendering clients can use this latency value to compute the minimum amount of data that they can write during any single processing pass. To write less than this minimum is to risk introducing glitches into the audio stream. For more information, see <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a>