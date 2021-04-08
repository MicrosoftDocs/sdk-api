---
UID: NF:icm.WcsGetDefaultColorProfile
title: WcsGetDefaultColorProfile
description: Retrieves the default color profile for a device, or for a device-independent default if the device is not specified.
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
 - WcsGetDefaultColorProfile
f1_keywords:
 - WcsGetDefaultColorProfile
 - icm/WcsGetDefaultColorProfile
dev_langs:
 - c++
---

## -description

Retrieves the default color profile for a device, or for a device-independent default if the device is not specified.

> [!NOTE] 
> This API does not support "advanced color" profiles for HDR monitors. Use [**ColorProfileGetDisplayDefault**](nf-icm-colorprofilegetdisplaydefault.md) for managing advanced color profiles.

## -parameters

### -param scope

A [**WCS_PROFILE_MANAGEMENT_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value specifying the scope of this profile management operation.

### -param pDeviceName

A pointer to the name of the device for which the default color profile is obtained. If **NULL**, a device-independent default profile is obtained.

### -param cptColorProfileType

A [**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype) value specifying the color profile type.

### -param cpstColorProfileSubType

A [**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype) value specifying the color profile subtype.

### -param dwProfileID

The ID of the color space that the color profile represents.

### -param cbProfileName

The buffer size, in bytes, of the buffer that is pointed to by *pProfileName*.

### -param pProfileName

A pointer to a buffer to receive the name of the color profile. The size of the buffer, in bytes, will be the indicated by *cbProfileName*.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

Use the [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) function to obtain the required size of the buffer that is pointed to by the *pProfileName* parameter.

If WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER is present, it overrides the system-wide default for *profileManagementScope*.

This function is executable in Least-Privileged User Account (LUA) context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [Functions](/windows/win32/wcs/functions)
* [COLORPROFILESUBTYPE](/windows/win32/api/icm/ne-icm-colorprofilesubtype)
* [COLORPROFILETYPE](/windows/win32/api/icm/ne-icm-colorprofiletype)
* [WCS_PROFILE_MANAGEMENT_SCOPE](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)
* [WcsGetDefaultColorProfileSize](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)
