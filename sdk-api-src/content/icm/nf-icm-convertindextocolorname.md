---
UID: NF:icm.ConvertIndexToColorName
title: ConvertIndexToColorName
description: Transforms indices in a color space to an array of names in a named color space. (ConvertIndexToColorName)
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
 - ConvertIndexToColorName
f1_keywords:
 - ConvertIndexToColorName
 - icm/ConvertIndexToColorName
dev_langs:
 - c++
---

## -description

Transforms indices in a color space to an array of names in a named color space.

## -parameters

### -param hProfile

The handle to an International Color Consortium (ICC) color space profile.

### -param paIndex

Pointer to an array of color-space index numbers. The indices begin with one, not zero.

### -param paColorName

Pointer to an array of color name structures.

### -param dwCount

The number of indices to convert.

## -returns

If this conversion function succeeds, the return value is **TRUE**.

If this conversion function fails, the return value is **FALSE**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because named profiles are explicit ICC profile types.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
