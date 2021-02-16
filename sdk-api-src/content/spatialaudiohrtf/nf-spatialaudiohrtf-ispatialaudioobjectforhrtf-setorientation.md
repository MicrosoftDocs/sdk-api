---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetOrientation
title: ISpatialAudioObjectForHrtf::SetOrientation (spatialaudiohrtf.h)
description: Sets the orientation in 3D space, relative to the listener's frame of reference, from which the ISpatialAudioObjectForHrtf audio data will be rendered.
helpviewer_keywords: ["ISpatialAudioObjectForHrtf interface [Core Audio]","SetOrientation method","ISpatialAudioObjectForHrtf.SetOrientation","ISpatialAudioObjectForHrtf::SetOrientation","SetOrientation","SetOrientation method [Core Audio]","SetOrientation method [Core Audio]","ISpatialAudioObjectForHrtf interface","coreaudio.ispatialaudioobjectforhrtf_setorientation","spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetOrientation"]
old-location: coreaudio\ispatialaudioobjectforhrtf_setorientation.htm
tech.root: CoreAudio
ms.assetid: 2B88643A-C81A-4F11-BFD0-EEF4C65861C8
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetOrientation method, ISpatialAudioObjectForHrtf.SetOrientation, ISpatialAudioObjectForHrtf::SetOrientation, SetOrientation, SetOrientation method [Core Audio], SetOrientation method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setorientation, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetOrientation
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
 - ISpatialAudioObjectForHrtf::SetOrientation
 - spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetOrientation
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
 - ISpatialAudioObjectForHrtf.SetOrientation
---

# ISpatialAudioObjectForHrtf::SetOrientation


## -description

Sets the orientation in 3D space, relative to the listener's frame of reference, from which the <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> audio data will be rendered.

## -parameters

### -param orientation [in]

An array of floats defining row-major 3x3 rotation matrix.

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

<a href="/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetOrientation</b>.

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

If <b>SetOrientation</b> is never called, the default value of an identity matrix is used. After <b>SetOrientation</b> is called, the orientation that is set will be used for the audio object until the orientation is changed with another call to <b>SetOrientation</b>.

## -see-also

<a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>