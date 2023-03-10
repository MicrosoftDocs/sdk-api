---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects
title: ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects (spatialaudioclient.h)
description: Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with ActivateSpatialAudioObject.
helpviewer_keywords: ["EndUpdatingAudioObjects","EndUpdatingAudioObjects method [Core Audio]","EndUpdatingAudioObjects method [Core Audio]","ISpatialAudioObjectRenderStreamBase interface","ISpatialAudioObjectRenderStreamBase interface [Core Audio]","EndUpdatingAudioObjects method","ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects","ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects","coreaudio.ispatialaudioobjectrenderstream_endupdatingaudioobjects","spatialaudioclient/ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects"]
old-location: coreaudio\ispatialaudioobjectrenderstream_endupdatingaudioobjects.htm
tech.root: CoreAudio
ms.assetid: 111DB695-66F6-45DD-B3B6-1DFB0D5D29FC
ms.date: 12/05/2018
ms.keywords: EndUpdatingAudioObjects, EndUpdatingAudioObjects method [Core Audio], EndUpdatingAudioObjects method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],EndUpdatingAudioObjects method, ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects, ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects, coreaudio.ispatialaudioobjectrenderstream_endupdatingaudioobjects, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects
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
 - ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects
 - spatialaudioclient/ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects
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
 - ISpatialAudioObjectRenderStreamBase.EndUpdatingAudioObjects
---

# ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects


## -description

Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ActivateSpatialAudioObject</a>.



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
<b>EndUpdatingAudioObjects</b> was called before <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">BeginUpdatingAudioObjects</a>.

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

The pointers retrieved with <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer">ISpatialAudioObjectBase::GetBuffer</a> can no longer be used after this method is called.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreambase">ISpatialAudioObjectRenderStreamBase</a>
