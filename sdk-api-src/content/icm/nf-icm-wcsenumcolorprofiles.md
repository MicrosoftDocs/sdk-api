---
UID: NF:icm.WcsEnumColorProfiles
title: WcsEnumColorProfiles
description: Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.
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
 - WcsEnumColorProfiles
f1_keywords:
 - WcsEnumColorProfiles
 - icm/WcsEnumColorProfiles
dev_langs:
 - c++
---

## -description

Enumerates color profiles associated with any device, in the specified scope.

> [!NOTE] 
> This API does not support "advanced color" profiles for HDR monitors. Use [**ColorProfileGetDisplayList**](nf-icm-colorprofilegetdisplaylist.md) for managing advanced color profiles.

## -parameters

### -param scope

A [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value specifying the scope of this profile management operation.

### -param pEnumRecord

A pointer to a structure specifying the enumeration criteria.

### -param pBuffer

A pointer to a buffer in which the profile names are to be enumerated. The **WcsEnumColorProfiles** function places, in this buffer, a MULTI\_SZ string that consists of profile names that satisfy the criteria specified in *\*pEnumRecord*.

### -param dwSize

A variable that contains the size, in bytes, of the buffer that is pointed to by *pBuffer*. See **Remarks**.

### -param pnProfiles

An optional pointer to a variable that receives the number of profile names that are copied to the buffer to which *pBuffer* points. Can be **NULL** if this information is not needed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

Use the [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) function to retrieve the value for the *dwSize* parameter, which is the size, in bytes, of the buffer pointed to by the *pBuffer* parameter.

If the *profileManagementScope* parameter is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_SYSTEM\_WIDE, only system-wide associations of profiles to the device are considered. If *profileManagementScope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, only per-user associations for the current user are considered. If [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles) has never been called for this user, or if **WcsSetUsePerUserProfiles** was most recently called for this user with its *usePerUserProfiles* parameter set to **FALSE**, then **WCSEnumColorProfiles** returns an empty list.

If WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER (the current user setting) is present, it overrides the system-wide default for the *profileManagementScope* parameter.

This function is executable in Least-Privileged User Account (LUA) context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [WCS_PROFILE_MANAGEMENT_SCOPE](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)
* [WcsEnumColorProfilesSize](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)
