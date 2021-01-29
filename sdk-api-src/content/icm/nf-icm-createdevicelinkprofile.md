---
UID: NF:icm.CreateDeviceLinkProfile
title: CreateDeviceLinkProfile
description: Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.
tech.root: wcs
ms.date: 01/26/2021
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
 - 
api_location:
 - Mscms.dll
api_name:
 - CreateDeviceLinkProfile
f1_keywords:
 - CreateDeviceLinkProfile
 - icm/CreateDeviceLinkProfile
dev_langs:
 - c++
---

## -description

Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.

## -parameters

### -param hProfile

Pointer to an array of handles of the color profiles to be used. The function determines whether the HPROFILEs contain ICC profile information and, if so, it processes them appropriately.

### -param nProfiles

Specifies the number of profiles in the array pointed to by *hProfile*.

### -param padwIntent

Pointer to an array of **DWORDS** containing the intents to be used. See [Rendering Intents](rendering-intents.md).

### -param nIntents

The number of intents in the array pointed to by *padwIntent*.

### -param dwFlags

Specifies flags to used control creation of the transform. For details, see [CMM Transform Creation Flags](cmm-transform-creation-flags.md).

### -param pProfileData

Pointer to a pointer to a buffer. If successful, this function allocates the buffer, places its address in *\*pProfileData*, and fills it with a device link profile. If the function succeeds, the calling application must free the buffer after it is no longer needed.

### -param indexPreferredCMM

Specifies the one-based index of the color profile that indicates what color management module (CMM) to use. The application developer may allow Windows to choose the CMM by setting this parameter to INDEX\_DONT\_CARE. See [Using Color Management Modules (CMM)](using-color-management-modules--cmm.md).

## -returns

If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero. For extended error information, call GetLastError.

## -remarks

For HPROFILEs that contain WCS profile information, the HPROFILEs are converted into valid ICC profile handles and then these ICC profile handles are used in creating the device link profile.

The first and the last profiles in the array must be device profiles. The other profiles can be color space or abstract profiles.

Each profile's output color space must be the next profile's input color space.

The calling application must free the buffer allocated by this function and pointed to by the *pProfileData* parameter. The [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree) function should be used to free the buffer.

## -see-also

* [Basic Color Management Concepts](ms536813\(v=vs.85\).md)
* [Functions](ms536536\(v=vs.85\).md)
* [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree)
