---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects
title: ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects (spatialaudioclient.h)
description: Puts the system into the state where audio object data can be submitted for processing and the ISpatialAudioObject state can be modified.
helpviewer_keywords: ["BeginUpdatingAudioObjects","BeginUpdatingAudioObjects method [Core Audio]","BeginUpdatingAudioObjects method [Core Audio]","ISpatialAudioObjectRenderStreamBase interface","ISpatialAudioObjectRenderStreamBase interface [Core Audio]","BeginUpdatingAudioObjects method","ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects","ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects","coreaudio.ispatialaudioobjectrenderstream_beginupdatingaudioobjects","spatialaudioclient/ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects"]
old-location: coreaudio\ispatialaudioobjectrenderstream_beginupdatingaudioobjects.htm
tech.root: CoreAudio
ms.assetid: 9D858556-2EBE-4DF6-878B-BE0E12079248
ms.date: 12/05/2018
ms.keywords: BeginUpdatingAudioObjects, BeginUpdatingAudioObjects method [Core Audio], BeginUpdatingAudioObjects method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],BeginUpdatingAudioObjects method, ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects, ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects, coreaudio.ispatialaudioobjectrenderstream_beginupdatingaudioobjects, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects
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
 - ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects
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
 - ISpatialAudioObjectRenderStreamBase.BeginUpdatingAudioObjects
---

# ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects


## -description

Puts the system into the state where audio object data can be submitted for processing and the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> state can be modified.

## -parameters

### -param availableDynamicObjectCount [out]

The number of dynamic audio objects that are available to be rendered for the current processing pass. All allocated static audio objects can be rendered in every pass. For information on audio object types, see <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a>.

### -param frameCountPerBuffer [out]

The size, in audio frames, of the buffer returned by <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer">GetBuffer</a>.

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
<dt><b>SPTLAUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
<b>BeginUpdatingAudioObjects</b> was called twice without a matching call to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">EndUpdatingAudioObjects</a> between the two calls.

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
<dt><b>AUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
A resource associated with the spatial audio stream is no longer valid.

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

This method must be called each time the event passed in the <a href="/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams">SpatialAudioObjectRenderStreamActivationParams</a> to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> is signaled,  
     even if there no audio object data to submit.

For each <b>BeginUpdatingAudioObjects</b> call, there should be a corresponding call to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">EndUpdatingAudioObjects</a> call.  
    If <b>BeginUpdatingAudioObjects</b> is called twice without a call <b>EndUpdatingAudioObjects</b> between them, the second call to  
    <b>BeginUpdatingAudioObjects</b> will return SPTLAUDCLNT_E_OUT_OF_ORDER.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>