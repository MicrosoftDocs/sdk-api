---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount
title: ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount (spatialaudioclient.h)
description: Gets the number of dynamic spatial audio objects that are currently available.
helpviewer_keywords: ["GetAvailableDynamicObjectCount","GetAvailableDynamicObjectCount method [Core Audio]","GetAvailableDynamicObjectCount method [Core Audio]","ISpatialAudioObjectRenderStreamBase interface","ISpatialAudioObjectRenderStreamBase interface [Core Audio]","GetAvailableDynamicObjectCount method","ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount","ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount","coreaudio.ispatialaudioobjectrenderstream_getavailabledynamicobjectcount","spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount"]
old-location: coreaudio\ispatialaudioobjectrenderstream_getavailabledynamicobjectcount.htm
tech.root: CoreAudio
ms.assetid: 5E17B53A-B999-4B08-9DFB-96D55E7F9CF7
ms.date: 12/05/2018
ms.keywords: GetAvailableDynamicObjectCount, GetAvailableDynamicObjectCount method [Core Audio], GetAvailableDynamicObjectCount method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],GetAvailableDynamicObjectCount method, ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount, ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount, coreaudio.ispatialaudioobjectrenderstream_getavailabledynamicobjectcount, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount
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
 - ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount
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
 - ISpatialAudioObjectRenderStreamBase.GetAvailableDynamicObjectCount
---

# ISpatialAudioObjectRenderStreamBase::GetAvailableDynamicObjectCount


## -description

Gets the number of dynamic spatial audio objects that are currently available.

## -parameters

### -param value [out]

The number of dynamic spatial audio objects that are currently available.

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
The audio device associated with the spatial audio stream is no longer valid.

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
<b>The media associated with the spatial audio stream uses an unsupported format.

</td>
</tr>

## -remarks

A dynamic <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is one that was activated by setting the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ActivateSpatialAudioObject</a> method to <b>AudioObjectType_Dynamic</b>. The system has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on an <b>ISpatialAudioObject</b>  when it is no longer being used to free up the resource to create new dynamic spatial audio objects.


You should not call this method after streaming has started, as the value is already provided by [ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects](./nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects.md). This method should only be called before streaming has started, which occurs after [ISpatialAudioObjectRenderStreamBase::Start](./nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start.md) is called.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>