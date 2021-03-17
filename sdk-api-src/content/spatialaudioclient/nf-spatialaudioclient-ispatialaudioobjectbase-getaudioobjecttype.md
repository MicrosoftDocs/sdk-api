---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.GetAudioObjectType
title: ISpatialAudioObjectBase::GetAudioObjectType (spatialaudioclient.h)
description: Gets a value specifying the type of audio object that is represented by the ISpatialAudioObject.
helpviewer_keywords: ["GetAudioObjectType","GetAudioObjectType method [Core Audio]","GetAudioObjectType method [Core Audio]","ISpatialAudioObjectBase interface","ISpatialAudioObjectBase interface [Core Audio]","GetAudioObjectType method","ISpatialAudioObjectBase.GetAudioObjectType","ISpatialAudioObjectBase::GetAudioObjectType","coreaudio.ispatialaudioobject_getaudioobjecttype","spatialaudioclient/ISpatialAudioObjectBase::GetAudioObjectType"]
old-location: coreaudio\ispatialaudioobject_getaudioobjecttype.htm
tech.root: CoreAudio
ms.assetid: C4FB5E8B-C80A-4B4B-9162-95B463543061
ms.date: 12/05/2018
ms.keywords: GetAudioObjectType, GetAudioObjectType method [Core Audio], GetAudioObjectType method [Core Audio],ISpatialAudioObjectBase interface, ISpatialAudioObjectBase interface [Core Audio],GetAudioObjectType method, ISpatialAudioObjectBase.GetAudioObjectType, ISpatialAudioObjectBase::GetAudioObjectType, coreaudio.ispatialaudioobject_getaudioobjecttype, spatialaudioclient/ISpatialAudioObjectBase::GetAudioObjectType
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
 - ISpatialAudioObjectBase::GetAudioObjectType
 - spatialaudioclient/ISpatialAudioObjectBase::GetAudioObjectType
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
 - ISpatialAudioObjectBase.GetAudioObjectType
---

# ISpatialAudioObjectBase::GetAudioObjectType


## -description

Gets a value specifying the type of audio object that is represented by the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>. This value indicates if the object is dynamic or static. If the object is static, one and only one of the static audio channel values to which the object is assigned is returned.

## -parameters

### -param audioObjectType [out]

A value specifying the type of audio object that is represented

## -returns

If the method succeeds, it returns S_OK.

## -remarks

Set the type of the audio object with the <i>type</i> parameter to the  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>