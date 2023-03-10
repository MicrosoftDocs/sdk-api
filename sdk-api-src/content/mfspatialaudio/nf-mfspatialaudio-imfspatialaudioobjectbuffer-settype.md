---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.SetType
title: IMFSpatialAudioObjectBuffer::SetType (mfspatialaudio.h)
description: Sets the type of the spatial audio object represented by the buffer.
helpviewer_keywords: ["IMFSpatialAudioObjectBuffer interface [Media Foundation]","SetType method","IMFSpatialAudioObjectBuffer.SetType","IMFSpatialAudioObjectBuffer::SetType","SetType","SetType method [Media Foundation]","SetType method [Media Foundation]","IMFSpatialAudioObjectBuffer interface","mf.imfspatialaudioobjectbuffer_settype","mfspatialaudio/IMFSpatialAudioObjectBuffer::SetType"]
old-location: mf\imfspatialaudioobjectbuffer_settype.htm
tech.root: mf
ms.assetid: 3D21D093-FDCE-4ECA-B8B2-56D6E5D5D9C6
ms.date: 12/05/2018
ms.keywords: IMFSpatialAudioObjectBuffer interface [Media Foundation],SetType method, IMFSpatialAudioObjectBuffer.SetType, IMFSpatialAudioObjectBuffer::SetType, SetType, SetType method [Media Foundation], SetType method [Media Foundation],IMFSpatialAudioObjectBuffer interface, mf.imfspatialaudioobjectbuffer_settype, mfspatialaudio/IMFSpatialAudioObjectBuffer::SetType
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSpatialAudioObjectBuffer::SetType
 - mfspatialaudio/IMFSpatialAudioObjectBuffer::SetType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer.SetType
---

# IMFSpatialAudioObjectBuffer::SetType


## -description

Sets the type of the spatial audio object represented by the buffer.

## -parameters

### -param type

A value from the <a href="/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype">AudioObjectType</a> enumeration specifying the type of audio object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A spatial audio object can be of type <b>AudioObjectType_Dynamic</b>, which means that it can change position and orientation in 3D space over time, or it can have a value such as <b>AudioObjectType_FrontLeft</b> which represents the static position of a real or virtual speaker that does not change position over time.

## -see-also

<a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a>