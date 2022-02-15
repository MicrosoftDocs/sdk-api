---
UID: NE:codecapi.eAVEncMPVSceneDetection
title: eAVEncMPVSceneDetection (codecapi.h)
description: Specifies how the encoder behaves when it detects a new scene. This enumeration is used with the AVEncMPVSceneDetection property.
helpviewer_keywords: ["codecapi/eAVEncMPVSceneDetection","codecapi/eAVEncMPVSceneDetection_InsertIPicture","codecapi/eAVEncMPVSceneDetection_None","codecapi/eAVEncMPVSceneDetection_StartNewGOP","codecapi/eAVEncMPVSceneDetection_StartNewLocatableGOP","dshow.eavencmpvscenedetection","eAVEncMPVSceneDetection","eAVEncMPVSceneDetection enumeration [DirectShow]","eAVEncMPVSceneDetectionEnumeration","eAVEncMPVSceneDetection_InsertIPicture","eAVEncMPVSceneDetection_None","eAVEncMPVSceneDetection_StartNewGOP","eAVEncMPVSceneDetection_StartNewLocatableGOP"]
old-location: dshow\eavencmpvscenedetection.htm
tech.root: dshow
ms.assetid: 81d273bd-06bc-4418-98af-8e7756aac91c
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVSceneDetection, codecapi/eAVEncMPVSceneDetection_InsertIPicture, codecapi/eAVEncMPVSceneDetection_None, codecapi/eAVEncMPVSceneDetection_StartNewGOP, codecapi/eAVEncMPVSceneDetection_StartNewLocatableGOP, dshow.eavencmpvscenedetection, eAVEncMPVSceneDetection, eAVEncMPVSceneDetection enumeration [DirectShow], eAVEncMPVSceneDetectionEnumeration, eAVEncMPVSceneDetection_InsertIPicture, eAVEncMPVSceneDetection_None, eAVEncMPVSceneDetection_StartNewGOP, eAVEncMPVSceneDetection_StartNewLocatableGOP
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - eAVEncMPVSceneDetection
 - codecapi/eAVEncMPVSceneDetection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncMPVSceneDetection
---

# eAVEncMPVSceneDetection enumeration


## -description

Specifies how the encoder behaves when it detects a new scene. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvscenedetection-property">AVEncMPVSceneDetection</a> property.

## -enum-fields

### -field eAVEncMPVSceneDetection_None:0

No special behavior.

### -field eAVEncMPVSceneDetection_InsertIPicture:1

Insert an I frame.

### -field eAVEncMPVSceneDetection_StartNewGOP:2

Start a new group of pictures (GOP).

### -field eAVEncMPVSceneDetection_StartNewLocatableGOP:3

Start a new GOP in which the first consecutive B frames do not reference the previous GOP.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
