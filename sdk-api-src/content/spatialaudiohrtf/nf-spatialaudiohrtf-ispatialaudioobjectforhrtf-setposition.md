---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectForHrtf.SetPosition
title: ISpatialAudioObjectForHrtf::SetPosition (spatialaudiohrtf.h)
description: Sets the position in 3D space, relative to the listener, from which the ISpatialAudioObjectForHrtf audio data will be rendered.
helpviewer_keywords: ["ISpatialAudioObjectForHrtf interface [Core Audio]","SetPosition method","ISpatialAudioObjectForHrtf.SetPosition","ISpatialAudioObjectForHrtf::SetPosition","SetPosition","SetPosition method [Core Audio]","SetPosition method [Core Audio]","ISpatialAudioObjectForHrtf interface","coreaudio.ispatialaudioobjectforhrtf_setposition","spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetPosition"]
old-location: coreaudio\ispatialaudioobjectforhrtf_setposition.htm
tech.root: CoreAudio
ms.assetid: 4FB6852D-A793-43A1-A58F-E7DCFDB5BBDD
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForHrtf interface [Core Audio],SetPosition method, ISpatialAudioObjectForHrtf.SetPosition, ISpatialAudioObjectForHrtf::SetPosition, SetPosition, SetPosition method [Core Audio], SetPosition method [Core Audio],ISpatialAudioObjectForHrtf interface, coreaudio.ispatialaudioobjectforhrtf_setposition, spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetPosition
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
 - ISpatialAudioObjectForHrtf::SetPosition
 - spatialaudiohrtf/ISpatialAudioObjectForHrtf::SetPosition
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
 - ISpatialAudioObjectForHrtf.SetPosition
---

# ISpatialAudioObjectForHrtf::SetPosition


## -description

Sets the position in 3D space, relative to the listener, from which the <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> audio data will be rendered.

## -parameters

### -param x [in]

The x position of the audio object, in meters, relative to the listener. Positive values are to the right of the listener and negative values are to the left.

### -param y [in]

The y position of the audio object, in meters, relative to the listener. Positive values are above the listener and negative values are below.

### -param z [in]

The z position of the audio object, in meters, relative to the listener. Positive values are behind the listener and negative values are in front.

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

<a href="/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetPosition</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b> SPTLAUDCLNT_E_PROPERTY_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> is not of type <b>AudioObjectType_Dynamic</b>. Set the type of the audio object with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf">ISpatialAudioObjectRenderStreamBase::ActivateSpatialAudioObjectForHrtf</a> method.

</td>
</tr>
</table>

## -remarks

This method can only be called on a  <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> that is of type <b>AudioObjectType_Dynamic</b>. Set the type of the audio object with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf">ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf</a> method.

 Position values use a right-handed Cartesian coordinate system, where each unit represents 1 meter. The coordinate system is relative to the listener where the origin (x=0.0, y=0.0, z=0.0) represents the center point between the listener's ears.

If <b>SetPosition</b> is never called, the origin (x=0.0, y=0.0, z=0.0) is used as the default position. After <b>SetPosition</b> is called, the position that is set will be used for the audio object until the position is changed with another call to <b>SetPosition</b>.

## -see-also

<a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a>