---
UID: NE:mfapi._eAVEncVideoQPMapElementDataType
tech.root: mf
title: eAVEncVideoQPMapElementDataType
ms.date: 12/09/2025
targetos: Windows
description: Specifies the data type of Quantization Parameter (QP) map values.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
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
 - mfapi.h
api_name:
 - _eAVEncVideoQPMapElementDataType
 - eAVEncVideoQPMapElementDataType
f1_keywords:
 - _eAVEncVideoQPMapElementDataType
 - mfapi/_eAVEncVideoQPMapElementDataType
 - eAVEncVideoQPMapElementDataType
 - mfapi/eAVEncVideoQPMapElementDataType
dev_langs:
 - c++
helpviewer_keywords:
 - _eAVEncVideoQPMapElementDataType
---

## -description

Specifies the data type of Quantization Parameter (QP) map values.

## -enum-fields

### -field CODEC_API_QP_MAP_INT8

QP map elements are of type **int8_t**.

### -field CODEC_API_QP_MAP_INT16

QP map elements are of type **int16_t**.

### -field CODEC_API_QP_MAP_INT32

QP map elements are of type **int32_t**.

### -field CODEC_API_QP_MAP_UINT8

QP map elements are of type **uint8_t**.

### -field CODEC_API_QP_MAP_UINT16

QP map elements are of type **uint16_t**.

### -field CODEC_API_QP_MAP_UINT32

QP map elements are of type **uint32_t**.

## -remarks

This enumeration is used by the *dataType* field of the [InputQPSettings](ns-mfapi-inputqpsettings.md) structure which provides data for the [CODECAPI_AVEncVideoInputAbsoluteQPBlockSettings](/windows/win32/medfound/codecapi-avencvideoinputabsoluteqpblocksettings) and [CODECAPI_AVEncVideoInputDeltaQPBlockSettings](/windows/win32/medfound/codecapi-avencvideoinputdeltaqpblocksettings) properties.

## -see-also

