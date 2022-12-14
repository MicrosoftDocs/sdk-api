---
UID: NF:icm.CreateProfileFromLogColorSpaceW
title: CreateProfileFromLogColorSpaceW
description: Converts a logical [color space](/windows/win32/wcs/c) to a [device profile](/windows/win32/wcs/d). (Unicode)
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
 - CreateProfileFromLogColorSpaceW
 - CreateProfileFromLogColorSpace
f1_keywords:
 - CreateProfileFromLogColorSpaceW
 - icm/CreateProfileFromLogColorSpaceW
 - CreateProfileFromLogColorSpace
 - icm/CreateProfileFromLogColorSpace
dev_langs:
 - c++
---

## -description

Converts a logical [color space](/windows/win32/wcs/color-spaces) to a [device profile](/windows/win32/wcs/using-device-profiles-with-wcs).

## -parameters

### -param pLogColorSpace

A pointer to a logical color space structure. See [**LOGCOLORSPACEA**](/windows/desktop/api/Wingdi/ns-wingdi-logcolorspacea) for details. The **lcsFilename** \[0\] member of the structure must be set to the **null** character ('\\0') or this function call will fail with the return value of INVALID\_PARAMETER.

### -param pProfile

A pointer to a pointer to a buffer where the device profile will be created. This function allocates the buffer and fills it with profile information if it is successful. If not, the pointer is set to **NULL**. The caller is responsible for freeing this buffer when it is no longer needed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**.

If the **lcsFilename** \[0\] member if the [**LOGCOLORSPACEA**](/windows/desktop/api/Wingdi/ns-wingdi-logcolorspacea) structure pointed to by *pLogColorSpace* is not '\\0', this function returns INVALID\_PARAMETER.

## -remarks

This function can be used with ASCII or Unicode strings. The buffer created by this function must be freed by the caller when it is no longer needed or there will be a memory leak. The [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree) function should be used to free this buffer.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree)
