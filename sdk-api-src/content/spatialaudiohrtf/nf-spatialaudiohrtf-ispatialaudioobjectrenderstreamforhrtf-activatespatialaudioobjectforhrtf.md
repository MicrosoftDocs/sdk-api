---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf
title: ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf (spatialaudiohrtf.h)
description: Activates an ISpatialAudioObjectForHrtf for audio rendering.
helpviewer_keywords: ["ActivateSpatialAudioObjectForHrtf","ActivateSpatialAudioObjectForHrtf method [Core Audio]","ActivateSpatialAudioObjectForHrtf method [Core Audio]","ISpatialAudioObjectRenderStreamForHrtf interface","ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio]","ActivateSpatialAudioObjectForHrtf method","ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf","ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf","coreaudio.ispatialaudiorenderstreamforhrtf_activatespatialaudioobjectforhrtf","spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf"]
old-location: coreaudio\ispatialaudiorenderstreamforhrtf_activatespatialaudioobjectforhrtf.htm
tech.root: CoreAudio
ms.assetid: 3E26D14B-5F69-4EBD-A48D-D63E24520D59
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioObjectForHrtf, ActivateSpatialAudioObjectForHrtf method [Core Audio], ActivateSpatialAudioObjectForHrtf method [Core Audio],ISpatialAudioObjectRenderStreamForHrtf interface, ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio],ActivateSpatialAudioObjectForHrtf method, ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf, ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf, coreaudio.ispatialaudiorenderstreamforhrtf_activatespatialaudioobjectforhrtf, spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf
req.header: spatialaudiohrtf.h
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
 - ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf
 - spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiohrtf.h
api_name:
 - ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf
---

# ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf


## -description

Activates an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> for audio rendering.

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

A dynamic <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> is one that was activated by setting the <i>type</i> parameter to the   <b>ActivateSpatialAudioObjectForHrtf</b> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. After the limit has been reached, attempting to activate additional audio objects will result in this method returning an SPTLAUDCLNT_E_NO_MORE_OBJECTS error. To avoid this, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on each dynamic <b>ISpatialAudioObjectForHrtf</b> after it is no longer being used to free up the resource so that it can be reallocated. See <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-isactive">ISpatialAudioObjectgBase::IsActive</a> and  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">ISpatialAudioObjectgBase::SetEndOfStream</a> for more information on the managing the lifetime of spatial audio objects.

## -see-also

<a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf">ISpatialAudioRenderStreamForHrtf</a>