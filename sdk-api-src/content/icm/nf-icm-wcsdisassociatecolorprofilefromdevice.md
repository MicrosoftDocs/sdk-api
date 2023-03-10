---
UID: NF:icm.WcsDisassociateColorProfileFromDevice
title: WcsDisassociateColorProfileFromDevice
description: Disassociates a specified WCS color profile from a specified device on a computer.
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
 - WcsDisassociateColorProfileFromDevice
f1_keywords:
 - WcsDisassociateColorProfileFromDevice
 - icm/WcsDisassociateColorProfileFromDevice
dev_langs:
 - c++
---

## -description

Disassociates a specified WCS color profile from a specified device on a computer.

> [!NOTE] 
> This API does not support "advanced color" profiles for HDR monitors. Use [**ColorProfileRemoveDisplayAssociation**](nf-icm-colorprofileremovedisplayassociation.md) for managing advanced color profiles.

## -parameters

### -param scope

A [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value that specifies the scope of this profile management operation, which could be system-wide or for the current user.

### -param pProfileName

A pointer to the file name of the profile to disassociate.

### -param pDeviceName

A pointer to the name of the device from which to disassociate the profile.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

The WCS color profile should be installed. Moreover, you must use the same *profileManagementScope* value as when the device was associated with the profile. See [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice).

If *profileManagementScope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_SYSTEM\_WIDE, the profile disassociation is systemwide and applies to all users. If *profileManagementScope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, the disassociation is only for the current user.

If more than one color profile is associated with a device, WCS uses the last associated profile as the default. For example, if your application sequentially associates three profiles with a device, WCS uses the last profile associated as the default. If your application then calls the **WcsDisassociateColorProfileFromDevice** function to disassociate the third profile (which is the default in this example), WCS uses the second profile as the default.

If your application disassociates all profiles from a device, WCS uses the sRGB profile as the default.

If *profileManagementScope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, this function is executable in Least-Privileged User Account (LUA) context. Otherwise, administrative privileges are required.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [WcsAssociateColorProfileWithDevice](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)
