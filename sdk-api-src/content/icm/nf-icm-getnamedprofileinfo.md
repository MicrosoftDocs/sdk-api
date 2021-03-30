---
UID: NF:icm.GetNamedProfileInfo
title: GetNamedProfileInfo
description: Retrieves information about the International Color Consortium (ICC) named color profile that is specified in the first parameter.
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
req.lib: Gdi32.lib
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
 - GetNamedProfileInfo
f1_keywords:
 - GetNamedProfileInfo
 - icm/GetNamedProfileInfo
dev_langs:
 - c++
---

## -description

Retrieves information about the International Color Consortium (ICC) named color profile that is specified in the first parameter.

## -parameters

### -param hProfile

The handle to the ICC profile from which the information will be retrieved.

### -param pNamedProfileInfo

A pointer to a **NAMED\_PROFILE\_INFO** structure.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because named profiles are explicit ICC profile types.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [NAMED\_PROFILE\_INFO](/windows/win32/api/icm/ns-icm-named_profile_info)
