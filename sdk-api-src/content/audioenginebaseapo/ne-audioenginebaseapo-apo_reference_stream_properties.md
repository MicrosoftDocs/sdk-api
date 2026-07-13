---
UID: NE:audioenginebaseapo.APO_REFERENCE_STREAM_PROPERTIES
tech.root: audio
title: APO_REFERENCE_STREAM_PROPERTIES
ms.date: 04/27/2023
targetos: Windows
description: Specifies loopback stream properties for the IApoAcousticEchoCancellation2::GetDesiredReferenceStreamProperties callback method.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioenginebaseapo.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22621
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioenginebaseapo.h
api_name:
 - APO_REFERENCE_STREAM_PROPERTIES
f1_keywords:
 - APO_REFERENCE_STREAM_PROPERTIES
 - audioenginebaseapo/APO_REFERENCE_STREAM_PROPERTIES
dev_langs:
 - c++
helpviewer_keywords:
 - APO_REFERENCE_STREAM_PROPERTIES
---

## -description

Specifies requested loopback stream properties.

## -enum-fields

### -field APO_REFERENCE_STREAM_PROPERTIES_NONE

No loopback stream properties.

### -field APO_REFERENCE_STREAM_PROPERTIES_POST_VOLUME_LOOPBACK

The loopback stream should be tapped after volume and/or mute are applied, if supported by the audio endpoint.

## -remarks

APOs request loopback stream properties by returning a bitwise combination of flags from this enumeration from an implementation of the [IApoAcousticEchoCancellation2::GetDesiredReferenceStreamProperties](nf-audioenginebaseapo-iapoacousticechocancellation2-getdesiredreferencestreamproperties.md) method.

## -see-also

