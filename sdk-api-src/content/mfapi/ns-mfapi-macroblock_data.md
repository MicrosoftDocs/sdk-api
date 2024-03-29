---
UID: NS:mfapi._MACROBLOCK_DATA
tech.root: mf
title: MACROBLOCK_DATA
ms.date: 03/29/2024
targetos: Windows
description: Provides data about a macroblock during video decoding.
prerelease: true
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
req.typenames: MACROBLOCK_DATA
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
 - _MACROBLOCK_DATA
 - MACROBLOCK_DATA
f1_keywords:
 - _MACROBLOCK_DATA
 - mfapi/_MACROBLOCK_DATA
 - MACROBLOCK_DATA
 - mfapi/MACROBLOCK_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _MACROBLOCK_DATA
---

## -description

Provides data about a macroblock during video decoding.

## -struct-fields

### -field flags

A bitwise OR combination of zero or more of the following values:

| Constant | Value | Description |
|----------|-------|-------------|
| MACROBLOCK_FLAG_SKIP | 0x00000001  | The macroblock is not needed for output and can be skipped. |
| MACROBLOCK_FLAG_DIRTY | 0x00000002 | The macroblock is changed from the previous frame. |
| MACROBLOCK_FLAG_MOTION | 0x00000004 | The macroblock from the previous frame has moved to a new position. |
| MACROBLOCK_FLAG_VIDEO | 0x00000008 | The macroblock contains video playback or other continuous motion, rather than a slower moving screen capture |
| MACROBLOCK_FLAG_HAS_MOTION_VECTOR | 0x00000010 | The motion vector values of the **MACROBLOCK_DATA** are valid, and should be used in preference to the encoder's calculated motion vector values |
| MACROBLOCK_FLAG_HAS_QP | 0x00000020 | The *QPDelta* value of the **MACROBLOCK_DATA** is valid, and specifies the QP of this macroblock relative to the rest of the frame. |

### -field motionVectorX

The X component of the motion vector of the macroblock.

### -field motionVectorY

The Y component of the motion vector of the macroblock.

### -field QPDelta

The delta quantization paramater value of the macroblock.

## -remarks

## -see-also

