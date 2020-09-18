---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.IsActive
title: ISpatialAudioObjectBase::IsActive (spatialaudioclient.h)
description: Gets a boolean value indicating whether the ISpatialAudioObject is valid.
helpviewer_keywords: ["ISpatialAudioObjectBase interface [Core Audio]","IsActive method","ISpatialAudioObjectBase.IsActive","ISpatialAudioObjectBase::IsActive","IsActive","IsActive method [Core Audio]","IsActive method [Core Audio]","ISpatialAudioObjectBase interface","coreaudio.ispatialaudioobject_isactive","spatialaudioclient/ISpatialAudioObjectBase::IsActive"]
old-location: coreaudio\ispatialaudioobject_isactive.htm
tech.root: CoreAudio
ms.assetid: 3339E021-4AC3-43CB-9306-C8D58541CA5F
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectBase interface [Core Audio],IsActive method, ISpatialAudioObjectBase.IsActive, ISpatialAudioObjectBase::IsActive, IsActive, IsActive method [Core Audio], IsActive method [Core Audio],ISpatialAudioObjectBase interface, coreaudio.ispatialaudioobject_isactive, spatialaudioclient/ISpatialAudioObjectBase::IsActive
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
 - ISpatialAudioObjectBase::IsActive
 - spatialaudioclient/ISpatialAudioObjectBase::IsActive
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
 - ISpatialAudioObjectBase.IsActive
---

# ISpatialAudioObjectBase::IsActive


## -description

Gets a boolean value indicating whether the <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a> is valid.

## -parameters

### -param isActive [out]

<b>TRUE</b> if the audio object is currently valid; otherwise, <b>FALSE</b>.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

If this value is false, you should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> to make the audio object resource available in the future.

<b>IsActive</b> will be set to false after <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream">SetEndOfStream</a> is called implicitly or explicitly. <b>SetEndOfStream</b> is called implicitly by the system if <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer">GetBuffer</a> is not called within an audio processing pass (between calls to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> and <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>).

The rendering engine will also deactivate the audio object, setting <b>IsActive</b> to false, when audio object resources become unavailable. In this case, a notification is sent via <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify">ISpatialAudioObjectRenderStreamNotify</a> before the object is deactivated. The value returned in the <i>availableDynamicObjectCount</i> parameter to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> indicates how many objects will be processed for each pass.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject">ISpatialAudioObject</a>



<a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>