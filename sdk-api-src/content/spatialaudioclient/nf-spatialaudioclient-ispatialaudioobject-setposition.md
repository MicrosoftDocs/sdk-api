---
UID: NF:spatialaudioclient.ISpatialAudioObject.SetPosition
title: ISpatialAudioObject::SetPosition (spatialaudioclient.h)
description: Sets the position in 3D space, relative to the listener, from which the ISpatialAudioObject audio data will be rendered.
helpviewer_keywords: ["ISpatialAudioObject interface [Core Audio]","SetPosition method","ISpatialAudioObject.SetPosition","ISpatialAudioObject::SetPosition","SetPosition","SetPosition method [Core Audio]","SetPosition method [Core Audio]","ISpatialAudioObject interface","coreaudio.ispatialaudioobject_setposition","spatialaudioclient/ISpatialAudioObject::SetPosition"]
old-location: coreaudio\ispatialaudioobject_setposition.htm
tech.root: CoreAudio
ms.assetid: DDF4859E-6510-45D5-82E7-2C5A7F2EC679
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObject interface [Core Audio],SetPosition method, ISpatialAudioObject.SetPosition, ISpatialAudioObject::SetPosition, SetPosition, SetPosition method [Core Audio], SetPosition method [Core Audio],ISpatialAudioObject interface, coreaudio.ispatialaudioobject_setposition, spatialaudioclient/ISpatialAudioObject::SetPosition
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
 - ISpatialAudioObject::SetPosition
 - spatialaudioclient/ISpatialAudioObject::SetPosition
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
 - ISpatialAudioObject.SetPosition
---

# ISpatialAudioObject::SetPosition


## -description

Sets the position in 3D space, relative to the listener, from which the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> audio data will be rendered.

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

<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetPosition</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> and <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> SPTLAUDCLNT_E_PROPERTY_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is not of type <b>AudioObjectType_Dynamic</b>. Set the type of the audio object with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStreamBase::ActivateSpatialAudioObject</a> method.

</td>
</tr>
</table>

## -remarks

This method can only be called on a  <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> that is of type <b>AudioObjectType_Dynamic</b>. Set the type of the audio object with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStreamBase::ActivateSpatialAudioObject</a> method.

 Position values use a right-handed Cartesian coordinate system, where each unit represents 1 meter. The coordinate system is relative to the listener where the origin (x=0.0, y=0.0, z=0.0) represents the center point between the listener's ears.

If <b>SetPosition</b> is never called, the origin (x=0.0, y=0.0, z=0.0) is used as the default position. After <b>SetPosition</b> is called, the position that is set will be used for the audio object until the position is changed with another call to <b>SetPosition</b>.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>