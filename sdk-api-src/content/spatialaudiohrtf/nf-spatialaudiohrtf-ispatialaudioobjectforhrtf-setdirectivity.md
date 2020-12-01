---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetDirectivity
title: ISpatialAudioObjectForHrtf::SetDirectivity (spatialaudiohrtf.h)
description: Sets the spatial audio directivity model for the ISpatialAudioObjectForHrtf.
helpviewer_keywords: ["ISpatialAudioObjectForHrtf interface [Core Audio]","SetDirectivity method","ISpatialAudioObjectForHrtf.SetDirectivity","ISpatialAudioObjectForHrtf::SetDirectivity","SetDirectivity","SetDirectivity method [Core Audio]","SetDirectivity method [Core Audio]","ISpatialAudioObjectForHrtf interface","coreaudio.ispatialaudioobjectforhrtf_setdirectivity","spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDirectivity"]
old-location: coreaudio\ispatialaudioobjectforhrtf_setdirectivity.htm
tech.root: CoreAudio
ms.assetid: 20934FA5-2B4E-4FC4-B5B5-AFC4024ED2F8
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetDirectivity method, ISpatialAudioObjectForHrtf.SetDirectivity, ISpatialAudioObjectForHrtf::SetDirectivity, SetDirectivity, SetDirectivity method [Core Audio], SetDirectivity method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setdirectivity, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDirectivity
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
 - ISpatialAudioObjectForHrtf::SetDirectivity
 - spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDirectivity
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
 - ISpatialAudioObjectForHrtf.SetDirectivity
---

# ISpatialAudioObjectForHrtf::SetDirectivity


## -description

Sets the spatial audio directivity model for the <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>.

## -parameters

### -param directivity

The spatial audio directivity model. This value can be one of the following structures:

<ul>
<li>
<a href="/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivity">SpatialAudioHrtfDirectivity</a>
</li>
<li>
<a href="/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivitycardioid">SpatialAudioHrtfDirectivityCardioid</a>
</li>
<li>
<a href="/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivitycone">SpatialAudioHrtfDirectivityCone</a>
</li>
</ul>

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

<a href="/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetDirectivity</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> and <a href="/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)">ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects</a>).

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivity">SpatialAudioHrtfDirectivity</a> structure represents an omnidirectional model that can be linearly interpolated with a cardioid or cone model.

If <b>SetDirectivity</b> is not called, the default type of <a href="/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfdirectivitytype">SpatialAudioHrtfDirectivity_OmniDirectional</a> is used with no interpolation.

## -see-also

<a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>