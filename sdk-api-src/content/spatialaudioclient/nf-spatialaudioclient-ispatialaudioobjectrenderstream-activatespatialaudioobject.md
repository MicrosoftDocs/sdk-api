---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStream.ActivateSpatialAudioObject
title: ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject (spatialaudioclient.h)
description: Activates an ISpatialAudioObject for audio rendering.
helpviewer_keywords: ["ActivateSpatialAudioObject","ActivateSpatialAudioObject method [Core Audio]","ActivateSpatialAudioObject method [Core Audio]","ISpatialAudioObjectRenderStream interface","ISpatialAudioObjectRenderStream interface [Core Audio]","ActivateSpatialAudioObject method","ISpatialAudioObjectRenderStream.ActivateSpatialAudioObject","ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject","coreaudio.ispatialaudioobjectrenderstream_activatespatialaudioobject","spatialaudioclient/ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject"]
old-location: coreaudio\ispatialaudioobjectrenderstream_activatespatialaudioobject.htm
tech.root: CoreAudio
ms.assetid: 1B99E7FB-0796-4902-9B00-470FD08F8AFA
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioObject, ActivateSpatialAudioObject method [Core Audio], ActivateSpatialAudioObject method [Core Audio],ISpatialAudioObjectRenderStream interface, ISpatialAudioObjectRenderStream interface [Core Audio],ActivateSpatialAudioObject method, ISpatialAudioObjectRenderStream.ActivateSpatialAudioObject, ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject, coreaudio.ispatialaudioobjectrenderstream_activatespatialaudioobject, spatialaudioclient/ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject
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
 - ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject
 - spatialaudioclient/ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject
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
 - ISpatialAudioObjectRenderStream.ActivateSpatialAudioObject
---

# ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject


## -description

Activates an <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> for audio rendering.

## -parameters

### -param type [in]

The type of audio object to activate. For dynamic audio objects, this value must be <b>AudioObjectType_Dynamic</b>. For static audio objects, specify one of the static audio channel values from the enumeration. Specifying <b>AudioObjectType_None</b> will produce an audio object that is not spatialized.

### -param audioObject [out]

Receives a pointer to the activated interface.

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
<dt><b>SPTLAUDCLNT_E_NO_MORE_OBJECTS </b></dt>
</dl>
</td>
<td width="60%">
The system has reached the maximum number of simultaneous audio objects.

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

A dynamic <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is one that was activated by setting the <i>type</i> parameter to the  <b>ActivateSpatialAudioObject</b> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. After the limit has been reached, attempting to activate additional audio objects will result in this method returning an SPTLAUDCLNT_E_NO_MORE_OBJECTS error. To avoid this, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on each dynamic <b>ISpatialAudioObject</b> after it is no longer being used to free up the resource so that it can be reallocated. See <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-isactive">ISpatialAudioObject::IsActive</a> and <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">ISpatialAudioObject::SetEndOfStream</a> for more information on the managing the lifetime of spatial audio objects.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>