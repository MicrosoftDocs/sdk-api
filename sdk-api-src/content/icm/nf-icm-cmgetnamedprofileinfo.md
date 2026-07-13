---
UID: NF:icm.CMGetNamedProfileInfo
title: CMGetNamedProfileInfo
description: Retrieves information about the specified named color profile.
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
 - CMGetNamedProfileInfo
f1_keywords:
 - CMGetNamedProfileInfo
 - icm/CMGetNamedProfileInfo
dev_langs:
 - c++
---

## -description

Retrieves information about the specified named color profile.

## -parameters

### -param hProfile

The handle to the profile from which the information will be retrieved.

### -param pNamedProfileInfo

A pointer to a **NAMED_PROFILE_INFO** structure.

## -returns

If this function succeeds, the return value is TRUE.

If this function fails, the return value is FALSE. When this occurs, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

This function is required in the default CMM. It is optional for all other CMMs.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [NAMED_PROFILE_INFO](/windows/win32/api/icm/ns-icm-named_profile_info)
