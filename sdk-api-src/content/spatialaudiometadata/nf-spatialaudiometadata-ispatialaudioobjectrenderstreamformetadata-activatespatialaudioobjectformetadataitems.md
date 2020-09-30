---
UID: NF:spatialaudiometadata.ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataItems
title: ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems (spatialaudiometadata.h)
description: Activate an ISpatialAudioObjectForMetadataItems for rendering.
helpviewer_keywords: ["ActivateSpatialAudioObjectForMetadataItems","ActivateSpatialAudioObjectForMetadataItems method [Core Audio]","ActivateSpatialAudioObjectForMetadataItems method [Core Audio]","ISpatialAudioObjectRenderStreamForMetadata interface","ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio]","ActivateSpatialAudioObjectForMetadataItems method","ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataItems","ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems","coreaudio.ispatialaudioobjectformetadataitems_activatespatialaudioobjectformetadataitems","coreaudio.ispatialaudioobjectrenderstreamformetadataitems_activatespatialaudioobjectformetadataitems","spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems"]
old-location: coreaudio\ispatialaudioobjectrenderstreamformetadataitems_activatespatialaudioobjectformetadataitems.htm
tech.root: CoreAudio
ms.assetid: A9743D42-659A-404C-BB21-8A5086870F34
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioObjectForMetadataItems, ActivateSpatialAudioObjectForMetadataItems method [Core Audio], ActivateSpatialAudioObjectForMetadataItems method [Core Audio],ISpatialAudioObjectRenderStreamForMetadata interface, ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio],ActivateSpatialAudioObjectForMetadataItems method, ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataItems, ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems, coreaudio.ispatialaudioobjectformetadataitems_activatespatialaudioobjectformetadataitems, coreaudio.ispatialaudioobjectrenderstreamformetadataitems_activatespatialaudioobjectformetadataitems, spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems
req.header: spatialaudiometadata.h
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
 - ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems
 - spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataItems
---

# ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems


## -description

Activate an <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a> for rendering.

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
<dt><b>SPTLAUDCLNT_E_NO_MORE_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of simultaneous spatial audio objects has been exceeded. Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on unused audio objects before attempting to activate additional objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_STATIC_OBJECT_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The static channel specified in the <i>type</i> parameter was not included in the <b>StaticObjectTypeMask</b> field of the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> passed into <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_OBJECT_ALREADY_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
A spatial audio object has already been activated for the static channel specified in the <i>type</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>type</i> parameter is not one of the values defined by the <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> enumeration.

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

A dynamic <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a> is one that was activated by setting the <i>type</i> parameter to the   <b>ActivateSpatialAudioObjectForMetadataItems</b> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. After the limit has been reached, attempting to activate additional audio objects will result in this method returning an SPTLAUDCLNT_E_NO_MORE_OBJECTS error. To avoid this, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on each dynamic <b>ISpatialAudioObjectForMetadataItems</b> after it is no longer being used to free up the resource so that it can be reallocated. See <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-isactive">ISpatialAudioObjectBase::IsActive</a> and  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">ISpatialAudioObjectBase::SetEndOfStream</a> for more information on the managing the lifetime of spatial audio objects.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a>