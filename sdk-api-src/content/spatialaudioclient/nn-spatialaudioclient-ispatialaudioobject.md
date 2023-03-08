---
UID: NN:spatialaudioclient.ISpatialAudioObject
title: ISpatialAudioObject (spatialaudioclient.h)
description: Represents an object that provides audio data to be rendered from a position in 3D space, relative to the user.
helpviewer_keywords: ["ISpatialAudioObject","ISpatialAudioObject interface [Core Audio]","ISpatialAudioObject interface [Core Audio]","described","coreaudio.ispatialaudioobject","spatialaudioclient/ISpatialAudioObject"]
old-location: coreaudio\ispatialaudioobject.htm
tech.root: CoreAudio
ms.assetid: EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObject, ISpatialAudioObject interface [Core Audio], ISpatialAudioObject interface [Core Audio],described, coreaudio.ispatialaudioobject, spatialaudioclient/ISpatialAudioObject
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ISpatialAudioObject
 - spatialaudioclient/ISpatialAudioObject
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
 - ISpatialAudioObject
---

# ISpatialAudioObject interface


## -description

Represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user. Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioObject</b> interface inherits from <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObject</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>
