---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetStaticObjectPosition
title: ISpatialAudioClient::GetStaticObjectPosition (spatialaudioclient.h)
description: Gets the position in 3D space of the specified static spatial audio channel.
helpviewer_keywords: ["GetStaticObjectPosition","GetStaticObjectPosition method [Core Audio]","GetStaticObjectPosition method [Core Audio]","ISpatialAudioClient interface","ISpatialAudioClient interface [Core Audio]","GetStaticObjectPosition method","ISpatialAudioClient.GetStaticObjectPosition","ISpatialAudioClient::GetStaticObjectPosition","coreaudio.ispatialaudioclient_getstaticobjectposition","spatialaudioclient/ISpatialAudioClient::GetStaticObjectPosition"]
old-location: coreaudio\ispatialaudioclient_getstaticobjectposition.htm
tech.root: CoreAudio
ms.assetid: F8CD558A-994D-46E0-98A0-1D7AD3B919C0
ms.date: 12/05/2018
ms.keywords: GetStaticObjectPosition, GetStaticObjectPosition method [Core Audio], GetStaticObjectPosition method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetStaticObjectPosition method, ISpatialAudioClient.GetStaticObjectPosition, ISpatialAudioClient::GetStaticObjectPosition, coreaudio.ispatialaudioclient_getstaticobjectposition, spatialaudioclient/ISpatialAudioClient::GetStaticObjectPosition
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
 - ISpatialAudioClient::GetStaticObjectPosition
 - spatialaudioclient/ISpatialAudioClient::GetStaticObjectPosition
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
 - ISpatialAudioClient.GetStaticObjectPosition
---

# ISpatialAudioClient::GetStaticObjectPosition


## -description

Gets the position in 3D space of the specified static spatial audio channel.

## -parameters

### -param type [in]

A value indicating the static spatial audio channel for which the position is being queried. This method will return E_INVALIDARG  if the value does not represent a static channel, including <b>AudioObjectType_Dynamic</b> and <b>AudioObjectType_None</b>.

### -param x [out]

The x coordinate of the static audio channel, in meters, relative to the listener. Positive values are to the right of the listener and negative values are to the left.

### -param y [out]

The y coordinate of the static audio channel, in meters, relative to the listener. Positive values are above the listener and negative values are below.

### -param z [out]

The z coordinate of the static audio channel, in meters, relative to the listener. Positive values are behind the listener and negative values are in front.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied  <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> value does not represent a static channel.

</td>
</tr>
</table>

## -remarks

 Position values use a right-handed Cartesian coordinate system, where each unit represents 1 meter. The coordinate system is relative to the listener where the origin (x=0.0, y=0.0, z=0.0) represents the center point between the listener's ears.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a>