---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.Start
title: ISpatialAudioObjectRenderStreamBase::Start (spatialaudioclient.h)
description: Starts the spatial audio stream.
helpviewer_keywords: ["ISpatialAudioObjectRenderStreamBase interface [Core Audio]","Start method","ISpatialAudioObjectRenderStreamBase.Start","ISpatialAudioObjectRenderStreamBase::Start","Start","Start method [Core Audio]","Start method [Core Audio]","ISpatialAudioObjectRenderStreamBase interface","coreaudio.ispatialaudioobjectrenderstream_start","spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Start"]
old-location: coreaudio\ispatialaudioobjectrenderstream_start.htm
tech.root: CoreAudio
ms.assetid: 25D968AC-F5D2-4CAB-87ED-29FC63E5A5A4
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase interface [Core Audio],Start method, ISpatialAudioObjectRenderStreamBase.Start, ISpatialAudioObjectRenderStreamBase::Start, Start, Start method [Core Audio], Start method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, coreaudio.ispatialaudioobjectrenderstream_start, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Start
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
 - ISpatialAudioObjectRenderStreamBase::Start
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase::Start
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
 - ISpatialAudioObjectRenderStreamBase.Start
---

# ISpatialAudioObjectRenderStreamBase::Start


## -description

Starts the spatial audio stream.



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
<dt><b>SPTLAUDCLNT_E_STREAM_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been stopped. Stop the stream by calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">Stop</a>.

</td>
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

Starting the stream causes data flow between the endpoint buffer and the audio engine.  
    The first time this method is called, the stream's audio clock position will be at 0.  
    Otherwise, the clock resumes from its position at the time that the stream was last paused with a call to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop">Stop</a>.  
Call <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset">Reset</a> to  reset the clock position to 0 and cause all active <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> instances to be revoked. 

The stream must have been previously stopped with a call to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop">Stop</a> or the method will fail and return SPTLAUDCLNT_E_STREAM_NOT_STOPPED.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>
