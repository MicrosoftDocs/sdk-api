---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.Stop
title: ISpatialAudioObjectRenderStreamBase::Stop (spatialaudioclient.h)
description: Stops a running audio stream.
helpviewer_keywords: ["ISpatialAudioObjectRenderStreamBase interface [Core Audio]","Stop method","ISpatialAudioObjectRenderStreamBase.Stop","ISpatialAudioObjectRenderStreamBase::Stop","Stop","Stop method [Core Audio]","Stop method [Core Audio]","ISpatialAudioObjectRenderStreamBase interface","coreaudio.ispatialaudioobjectrenderstream_stop","spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Stop"]
old-location: coreaudio\ispatialaudioobjectrenderstream_stop.htm
tech.root: CoreAudio
ms.assetid: 6ECD17AB-C37D-4F4E-9D7F-EC48FC3B838C
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase interface [Core Audio],Stop method, ISpatialAudioObjectRenderStreamBase.Stop, ISpatialAudioObjectRenderStreamBase::Stop, Stop, Stop method [Core Audio], Stop method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, coreaudio.ispatialaudioobjectrenderstream_stop, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Stop
req.header: spatialaudioclient.h
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
 - ISpatialAudioObjectRenderStreamBase::Stop
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Stop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.Stop
---

# ISpatialAudioObjectRenderStreamBase::Stop


## -description

Stops a running audio stream.



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
<dt><b>SPTLAUDCLNT_E_DESTROYED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a> associated with the spatial audio stream has been destroyed.

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
<dt><b>SPTLAUDCLNT_E_INTERNAL</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>



<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_UNSUPPORTED_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The media associated with the spatial audio stream uses an unsupported format.

</td>
</tr>
</table>

## -remarks

 Stopping stream causes data to stop flowing between the endpoint buffer and the audio engine.  
    You can consider this operation to pause the stream because it leaves the stream's audio clock at its current stream position and does not reset it to 0. A subsequent call to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start">Start</a> causes the stream to resume running from the current position.  
    Call <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset">Reset</a> to  reset the clock position to 0 and cause all active <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> instances to be revoked.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>
