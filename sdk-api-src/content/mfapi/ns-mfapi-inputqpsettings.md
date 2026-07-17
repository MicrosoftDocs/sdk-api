---
UID: NS:mfapi._inputQPSettings
tech.root: mf
title: InputQPSettings
ms.date: 12/11/2025
targetos: Windows
description: Describes the Quantization Parameter (QP) map settings that a video encoder MFT accepts as input.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: InputQPSettings
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - _inputQPSettings
 - InputQPSettings
f1_keywords:
 - _inputQPSettings
 - mfapi/_inputQPSettings
 - InputQPSettings
 - mfapi/InputQPSettings
dev_langs:
 - c++
helpviewer_keywords:
 - _inputQPSettings
---

## -description

Describes the Quantization Parameter (QP) map settings that a video encoder MFT accepts as input.

## -struct-fields

### -field minBlockSize

The minimum block size granularity at which the MFT can accept QP values.

### -field maxBlockSize

The maximum block size granularity at which the MFT can accept QP values.

### -field stepsBlockSize

An incremental step that can be added to *minBlockSize* to produce a block size. The resulting block size must be within the range [*minBlockSize*, *maxBlockSize*]. Zero is a possible value for *stepsBlockSize* which implies that *minBlockSize* and *maxBlockSize* are the only allowed values for the block size.

### -field dataType

A value from the [AVEncVideoQPMapElementDataType](eAVEncVideoQPMapElementDataType) specifying the data width and the signed nature of the QP min and max values.

### -field minValue

This value represents the minimum QP value accepted by the video encoder MFT. Any entry within such a QP map must be greater than or equal to *minValue*.

### -field maxValue

This value represents the maximum QP value accepted by the video encoder MFT. Any entry within such a QP map must be less than or equal to *maxValue*.

### -field step

An incremental step that can be added to *minValue* to produce a QP value. The resulting QP value must be within the range [*minValue*, *maxValue*]. Zero is a possible value for *step*, which implies that *minValue* and *maxValue* are the only allowed values for the QP value.

## -remarks

This structure provides data for the [CODECAPI_AVEncVideoInputAbsoluteQPBlockSettings](/windows/win32/medfound/codecapi-avencvideoinputabsoluteqpblocksettings) and [CODECAPI_AVEncVideoInputDeltaQPBlockSettings](/windows/win32/medfound/codecapi-avencvideoinputdeltaqpblocksettings) properties.

## -see-also

