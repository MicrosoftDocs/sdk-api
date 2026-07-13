---
UID: NF:icm.CMConvertIndexToColorName
title: CMConvertIndexToColorName
tech.root: wcs
description: Transforms indices in a color space to an array of names in a named color space. (CMConvertIndexToColorName)
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
 - icm.h
api_name:
 - CMConvertIndexToColorName
f1_keywords:
 - CMConvertIndexToColorName
 - icm/CMConvertIndexToColorName
dev_langs:
 - c++
---

## -description

Transforms indices in a color space to an array of names in a named color space.

## -parameters

### -param hProfile

The handle to a color space profile.

### -param paIndex

Pointer to an array of color-space index numbers.

### -param paColorName

Pointer to an array of color name structures.

### -param dwCount

The number of indices to convert.

## -returns

If this conversion function succeeds, the return value is TRUE.

If this function fails, the return value is FALSE. When this occurs, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

This function is required in the default CMM. It is optional for all other CMMs.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
