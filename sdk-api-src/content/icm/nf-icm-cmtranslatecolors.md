---
UID: NF:icm.CMTranslateColors
title: CMTranslateColors
description: Translates an array of colors from a source [color space](/windows/win32/wcs/c) to a destination color space using a color transform.
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
 - CMTranslateColors
f1_keywords:
 - CMTranslateColors
 - icm/CMTranslateColors
dev_langs:
 - c++
---

## -description

Translates an array of colors from a source [color space](/windows/win32/wcs/color-spaces) to a destination color space using a color transform.

## -parameters

### -param hcmTransform

Specifies the color transform to use.

### -param lpaInputColors

Points to an array of [**COLOR**](/windows/win32/api/icm/ns-icm-color) structures to translate.

### -param nColors

Specifies the number of elements in the array.

### -param ctInput

Specifies the color type of the input.

### -param lpaOutputColors

Points to a buffer in which an array of translated **COLOR** structures is to be placed.

### -param ctOutput

Specifies the output color type.

## -returns

If this function succeeds, the return value is TRUE.

If this function fails, the return value is FALSE. The CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

Every CMM is required to export this function.

If the input and the output color types are not compatible with the color transform, this function should fail.

Note that this function must support in-place translation. That is, whenever the memory footprint of the output is less than or equal to the memory footprint of the input, this function must be able to translate the bitmap colors even if the source and destination buffers are the same.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
