---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetGain
title: ISpatialAudioObjectForHrtf::SetGain (spatialaudiohrtf.h)
description: Sets the gain for the ISpatialAudioObjectForHrtf.
helpviewer_keywords: ["ISpatialAudioObjectForHrtf interface [Core Audio]","SetGain method","ISpatialAudioObjectForHrtf.SetGain","ISpatialAudioObjectForHrtf::SetGain","SetGain","SetGain method [Core Audio]","SetGain method [Core Audio]","ISpatialAudioObjectForHrtf interface","coreaudio.ispatialaudioobjectforhrtf_setgain","spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetGain"]
old-location: coreaudio\ispatialaudioobjectforhrtf_setgain.htm
tech.root: CoreAudio
ms.assetid: 7DE268DC-5AA0-4866-8495-34292AEFB142
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetGain method, ISpatialAudioObjectForHrtf.SetGain, ISpatialAudioObjectForHrtf::SetGain, SetGain, SetGain method [Core Audio], SetGain method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setgain, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetGain
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
 - ISpatialAudioObjectForHrtf::SetGain
 - spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetGain
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
 - ISpatialAudioObjectForHrtf.SetGain
---

# ISpatialAudioObjectForHrtf::SetGain


## -description

Sets the gain for the <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> in dB.

## -parameters

### -param gain [in]

The gain for the <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> in dB.

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

<a href="/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetGain</b>.

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

This is valid only for spatial audio objects configured to use the <a href="/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfdistancedecaytype">SpatialAudioHrtfDistanceDecay_CustomDecay</a> decay type. Set the decay type of an <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> object by calling <a href="/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setdistancedecay">SetDistanceDecay</a>. Set the default decay type for an all objects in an HRTF render stream by setting the <b>DistanceDecay</b> field of the <a href="/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams">SpatialAudioHrtfActivationParams</a> passed into <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a>.

If <b>SetGain</b> is never called, the default value of 0.0 is used. After <b>SetGain</b> is called, the gain that is set will be used for the audio object until the gain is changed with another call to <b>SetGain</b>.

## -see-also

<a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>