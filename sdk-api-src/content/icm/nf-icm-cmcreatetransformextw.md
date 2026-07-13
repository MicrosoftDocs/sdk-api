---
UID: NF:icm.CMCreateTransformExtW
title: CMCreateTransformExtW
description: Creates a color transform that maps from an input [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) to an optional target space and then to an output device, using a set of flags that define how the transform should be created.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - icm32.dll
api_name:
 - CMCreateTransformExtW
f1_keywords:
 - CMCreateTransformExtW
 - icm/CMCreateTransformExtW
dev_langs:
 - c++
---

## -description

Creates a color transform that maps from an input [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) to an optional target space and then to an output device, using a set of flags that define how the transform should be created.

## -parameters

### -param lpColorSpace

Pointer to an input logical color space structure.

### -param lpDevCharacter

Pointer to a memory-mapped device profile.

### -param lpTargetDevCharacter

Pointer to a memory-mapped target profile.

### -param dwFlags

Specifies flags to used control creation of the transform. For details, see [CMM transform creation flags](/windows/win32/wcs/cmm-transform-creation-flags).

## -returns

If this function succeeds, the return value is a color transform in the range 256 to 65,535. Since only the low **WORD** of the transform is retained, valid transforms cannot exceed this range.

If this function fails, the return value is an error code having a value less than 256. When the return value is less than 256, signaling an error, the CMM should use **SetLastError** to set the last error to a valid error value as defined in Winerror.h.

## -remarks

Every CMM is required to export this function.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CMCreateTransformExtW](/windows/win32/api/icm/nf-icm-cmcreatetransformextw)
