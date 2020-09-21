---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetDistanceDecay
title: ISpatialAudioObjectForHrtf::SetDistanceDecay (spatialaudiohrtf.h)
description: Sets the decay model that is applied over distance from the position of an ISpatialAudioObjectForHrtf to the position of the listener.
helpviewer_keywords: ["ISpatialAudioObjectForHrtf interface [Core Audio]","SetDistanceDecay method","ISpatialAudioObjectForHrtf.SetDistanceDecay","ISpatialAudioObjectForHrtf::SetDistanceDecay","SetDistanceDecay","SetDistanceDecay method [Core Audio]","SetDistanceDecay method [Core Audio]","ISpatialAudioObjectForHrtf interface","coreaudio.ispatialaudioobjectforhrtf_setdistancedecay","spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDistanceDecay"]
old-location: coreaudio\ispatialaudioobjectforhrtf_setdistancedecay.htm
tech.root: CoreAudio
ms.assetid: 62C95E6A-C27E-4C17-91E1-D6D80172F15B
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetDistanceDecay method, ISpatialAudioObjectForHrtf.SetDistanceDecay, ISpatialAudioObjectForHrtf::SetDistanceDecay, SetDistanceDecay, SetDistanceDecay method [Core Audio], SetDistanceDecay method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setdistancedecay, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDistanceDecay
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
 - ISpatialAudioObjectForHrtf::SetDistanceDecay
 - spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetDistanceDecay
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
 - ISpatialAudioObjectForHrtf.SetDistanceDecay
---

# ISpatialAudioObjectForHrtf::SetDistanceDecay


## -description

Sets the decay model that is applied over distance from the position of an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> to the position of the listener.

## -parameters

### -param distanceDecay [in]

The decay model.

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

<a href="/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetDistanceDecay</b>.

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

If <b>SetEnvironment</b> is not called, the default values are used.

## -see-also

<a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>