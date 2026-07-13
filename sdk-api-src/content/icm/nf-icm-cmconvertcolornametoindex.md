---
UID: NF:icm.CMConvertColorNameToIndex
title: CMConvertColorNameToIndex
description: Converts color names in a named color space to index numbers in a color profile.
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
 - icm.h
api_name:
 - CMConvertColorNameToIndex
f1_keywords:
 - CMConvertColorNameToIndex
 - icm/CMConvertColorNameToIndex
dev_langs:
 - c++
---

## -description

Converts color names in a named color space to index numbers in a color profile.

## -parameters

### -param hProfile

The handle to a named color profile.

### -param paColorName

Pointer to an array of color name structures.

### -param paIndex

Pointer to an array of **DWORDS** that this function fills with the indices.

### -param dwCount

The number of color names to convert.

## -returns

If this function succeeds with the conversion, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. When this occurs, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

This function is required in the default CMM. It is optional for all other CMMs.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
