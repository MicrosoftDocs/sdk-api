---
UID: NF:icm.CMCreateDeviceLinkProfile
title: CMCreateDeviceLinkProfile
description: Creates a [device link profile](/windows/win32/wcs/d) in the format specified by the International Color Consortium in its ICC Profile Format Specification.
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
 - CMCreateDeviceLinkProfile
f1_keywords:
 - CMCreateDeviceLinkProfile
 - icm/CMCreateDeviceLinkProfile
dev_langs:
 - c++
---

## -description

Creates a [device link profile](/windows/win32/wcs/d) in the format specified by the International Color Consortium in its ICC Profile Format Specification.

## -parameters

### -param pahProfiles

Pointer to an array of profile handles.

### -param nProfiles

Specifies the number of profiles in the array.

### -param padwIntents

An array of rendering intents.

### -param nIntents

The number of elements in the array of intents.

### -param dwFlags

Specifies flags to used control creation of the transform. For details, see [CMM Transform Creation Flags](/windows/win32/wcs/cmm-transform-creation-flags).

### -param lpProfileData

Pointer to a pointer to a buffer. If successful the function allocates and fills this buffer. The calling application must free this buffer when it is no longer needed. Use the **GlobalFree** function to free this buffer.

## -returns

If the function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero. If the function is not successful, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

Only the Windows default CMM is required to export this function; it is optional for all other CMMs.

If a CMM does not support **CMCreateDeviceLinkProfile**, Windows uses the default CMM to create a device link profile.

The first and the last profiles in the array must be [device profiles](/windows/win32/wcs/using-device-profiles-with-wcs). The other profiles can be [color space](/windows/win32/wcs/color-spaces) or abstract profiles. Each profile's output color space must be the next profile's input color space.

The calling application must free the buffer allocated by this function and pointed to by the *lpProfileData* parameter. Use the [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree) function to free the buffer.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree)
