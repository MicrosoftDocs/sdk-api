---
UID: NF:icm.WcsAssociateColorProfileWithDevice
title: WcsAssociateColorProfileWithDevice
description: WcsAssociateColorProfileWithDevice associates a specified WCS color profile with a specified device.
tech.root: wcs
ms.date: 08/03/2022
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
 - WcsAssociateColorProfileWithDevice
f1_keywords:
 - WcsAssociateColorProfileWithDevice
 - icm/WcsAssociateColorProfileWithDevice
dev_langs:
 - c++
---

## -description

Associates a specified WCS color profile with a specified device.

> [!NOTE] 
> This API does not support "advanced color" profiles for HDR monitors. Use [**ColorProfileAddDisplayAssociation**](nf-icm-colorprofileadddisplayassociation.md) for managing advanced color profiles.

## -parameters

### -param scope

A [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value that specifies the scope of this profile management operation, which could be system-wide or for the current user.

### -param pProfileName

A pointer to the file name of the profile to associate.

### -param pDeviceName

A pointer to the name of the device with which the profile is to be associated.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

The **WCSAssociateColorProfileWithDevice** function fails if the profile has not been installed on the computer using the [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) function.

If the *profileManagementScope* parameter is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_SYSTEM\_WIDE, the profile association is system-wide and applies to all users. If *profileManagementScope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, the association is only for the current user.

This function is executable in Least-Privileged User Account (LUA) context if *profileManagementScope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER. Otherwise, administrative privileges are required.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)
