---
UID: NS:audioapotypes.APO_CONNECTION_PROPERTY_V2
tech.root: coreaudio
title: APO_CONNECTION_PROPERTY_V2
ms.date: 02/17/2021
ms.topic: language-reference
targetos: Windows
description: Contains the dynamically changing connection properties. Version two of this structure introduces a time stamp that can be used to synchronize an auxiliary reference stream initialized with IApoAuxiliaryInputConfiguration. 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioapotypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.typenames: APO_CONNECTION_PROPERTY_V2
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioapotypes.h
api_name:
 - APO_CONNECTION_PROPERTY_V2
f1_keywords:
 - APO_CONNECTION_PROPERTY_V2
 - audioapotypes/APO_CONNECTION_PROPERTY_V2
helpviewer_keywords:
 - APO_CONNECTION_PROPERTY_V2
 - audioapotypes/APO_CONNECTION_PROPERTY_V2
dev_langs:
 - c++
---

## -description

Contains the dynamically changing connection properties. Version two of this structure introduces a time stamp that can be used to synchronize an auxiliary reference stream initialized with [IApoAuxiliaryInputConfiguration](../audioenginebaseapo/nn-audioenginebaseapo-iapoauxiliaryinputconfiguration.md). 

## -struct-fields

### -field property

A [APO_CONNECTION_PROPERTY](ns-audioapotypes-apo_connection_property.md) structure containing the version 1 properties.

### -field u64QPCTime

An unsigned 64-bit value representing a [QueryPerformanceCounter](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) time stamp for an audio buffer.

## -remarks
If the **u32Signature** field of the [APO_CONNECTION_PROPERTY](ns-audioapotypes-apo_connection_property.md) structure passed into [IAudioProcessingObjectRT::APOProcess](../audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectrt-apoprocess.md) is equal to **APO_CONNECTION_PROPERTY_V2_SIGNATURE**, the structure can be safely typecast to a **APO_CONNECTION_PROPERTY_V2**.

This structure was introduced to support acoustic echo cancellation scenarios. For more information, see [IApoAcousticEchoCancellation](../audioenginebaseapo/nn-audioenginebaseapo-iapoacousticechocancellation.md).

## -see-also
[APO_CONNECTION_PROPERTY](ns-audioapotypes-apo_connection_property.md)
[IApoAcousticEchoCancellation](../audioenginebaseapo/nn-audioenginebaseapo-iapoacousticechocancellation.md).
[APOProcess](../audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectrt-apoprocess.md)
