---
UID: NF:icm.GetStandardColorSpaceProfileA
title: GetStandardColorSpaceProfileA
description: Retrieves the color profile registered for the specified standard [color space](/windows/win32/wcs/c). (ANSI)
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
 - Mscms.dll
api_name:
 - GetStandardColorSpaceProfileA
 - GetStandardColorSpaceProfile
f1_keywords:
 - GetStandardColorSpaceProfileA
 - icm/GetStandardColorSpaceProfileA
 - GetStandardColorSpaceProfile
 - icm/GetStandardColorSpaceProfile
dev_langs:
 - c++
---

## -description

Retrieves the color profile registered for the specified standard [color space](/windows/win32/wcs/c#color-space).

## -parameters

### -param pMachineName

Reserved. Must be **NULL**. This parameter is intended to point to the name of the computer on which to get a standard color space profile. A **NULL** pointer indicates the local machine.

### -param dwSCS

Specifies the ID value of the standard color space for which to retrieve the profile. The only valid values for this parameter are LCS\_sRGB and LCS\_WINDOWS\_COLOR\_SPACE.

### -param pBuffer

Pointer to the buffer in which the name of the profile is to be placed. If **NULL**, the call will return **TRUE** and the required size of the buffer is placed in *pdwSize.*

### -param pcbSize

Pointer to a variable containing the size in bytes of the buffer pointed to by *pProfileName*. On return, the variable contains the size of the buffer actually used or needed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the buffer pointed to by *pProfileName* is to be dynamically allocated by an application, the application can call the **GetStandardColorSpaceProfile** function to retrieve the size required for the buffer. If **GetStandardColorSpaceProfile** is called with *pProfileName* set to **NULL**, it will return **FALSE** and the **DWORD** pointed at by *pdwSize* will contain the number of bytes needed for the buffer pointed at by *pProfileName*. The application can then allocate the buffer and call **GetStandardColorSpaceProfile** again with *pProfileName* set to the address of the buffer.

This function supports Windows Color System (WCS) device model profiles (DMPs) in addition to International Color Consortium (ICC) profiles. It does not support WCS CAMP or GMMP profiles and will return an error if such profiles are used.

**Overview of Windows Vista Specific Functionality**

This will support WCS DMPs in addition to ICC profiles. It will not support WCS CAMP or GMMP profiles and will return an error if such profiles are used with this API.

***Per-user/LUA support***

This will retrieve the color profile registered for the given standard color space for current user. If there is no such setting for the current user, it retrieves the system wide setting.

This uses **WcsGetDefaultColorProfile** with WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER.

This is executable in LUA context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [SetStandardColorSpaceProfile](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew)
