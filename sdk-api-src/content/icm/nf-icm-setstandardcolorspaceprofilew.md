---
UID: NF:icm.SetStandardColorSpaceProfileW
title: SetStandardColorSpaceProfileW
description: Registers a specified profile for a given standard [color space](/windows/win32/wcs/c). The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). (Unicode)
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
 - SetStandardColorSpaceProfileW
 - SetStandardColorSpaceProfile
f1_keywords:
 - SetStandardColorSpaceProfileW
 - icm/SetStandardColorSpaceProfileW
 - SetStandardColorSpaceProfile
 - icm/SetStandardColorSpaceProfile
dev_langs:
 - c++
---

## -description

Registers a specified profile for a given standard [color space](/windows/win32/wcs/c#color-space). The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).

## -parameters

### -param pMachineName

Reserved. Must be **NULL**. This parameter is intended to point to the name of the machine on which to set a standard color space profile. A **NULL** pointer indicates the local machine.

### -param dwProfileID

Specifies the ID value of the standard color space that the given profile represents. This is a custom ID value used to uniquely identify the color space profile within your application.

### -param pProfilename

Points to a fully qualified path to the profile file.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The profile must already be installed on the system before it can be registered for a standard color space.

This function supports Windows Color System (WCS) device model profiles (DMPs) in addition to International Color Consortium (ICC) profiles. It does not support WCS CAMP or GMMP profiles and will return an error if such profiles are used.

***Per-user/LUA support***

This will register a specified profile for a given standard color space only for current user.

This uses **WcsSetDefaultColorProfile** with WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER.

This is executable in LUA context if the profile is already installed, fails otherwise with access denied since install is system-wide and requires administrator privileges.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [SetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew)
