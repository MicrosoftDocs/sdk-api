---
UID: NF:icm.ConvertColorNameToIndex
title: ConvertColorNameToIndex
description: Converts color names in a named color space to index numbers in an International Color Consortium (ICC) color profile.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
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
 - mscms.dll
api_name:
 - ConvertColorNameToIndex
f1_keywords:
 - ConvertColorNameToIndex
 - icm/ConvertColorNameToIndex
dev_langs:
 - c++
---

## -description

Converts color names in a named color space to index numbers in an International Color Consortium (ICC) color profile.

## -parameters

### -param hProfile

The handle to an ICC named color profile.

### -param paColorName

Pointer to an array of color name structures.

### -param paIndex

Pointer to an array of **DWORDS** that this function fills with the indices. The indices begin with one, not zero.

### -param dwCount

The number of color names to convert.

## -returns

If this function succeeds with the conversion, the return value is **TRUE**.

If the conversion function fails, the return value is **FALSE**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because named profiles are explicit ICC profile types.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
