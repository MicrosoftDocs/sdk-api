---
UID: NF:icm.GetColorDirectoryA
title: GetColorDirectoryA
description: Retrieves the path of the Windows COLOR directory on a specified machine. (ANSI)
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
 - GetColorDirectoryA
 - GetColorDirectory
f1_keywords:
 - GetColorDirectoryA
 - icm/GetColorDirectoryA
 - GetColorDirectory
 - icm/GetColorDirectory
dev_langs:
 - c++
---

## -description

> [!NOTE] 
> This API may be unavailable in future releases. We encourage new and existing software to use other APIs for color profile interactions. Please refer to the below table for some examples.
>
>| Scenario | Mechanism |
>| :------: | :------: |
>|   Enumerating all installed profiles  |   Use [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) and [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles), or [**EnumColorProfilesA**](/windows/win32/api/icm/nf-icm-EnumColorProfilesA)  |
>|   Installing/Uninstalling color profiles  |   Use [**InstallColorProfileA**](/windows/win32/api/icm/nf-icm-InstallColorProfileA)/[**UninstallColorProfileA**](/windows/win32/api/icm/nf-icm-UninstallColorProfileA)  |
>|   Opening a color profile file directly  |   Use [**OpenColorProfileA**](/windows/win32/api/icm/nf-icm-OpenColorProfileA) with dwType=PROFILE_FILENAME in the PROFILE struct parameter.<br/> Or use [**WcsOpenColorProfileA**](/windows/win32/api/icm/nf-icm-WcsOpenColorProfileA). [**Icm.h**](/windows/win32/api/icm) contains many APIs that accept the returned HPROFILE for color profile manipulation  |

<br/>

Retrieves the path of the Windows COLOR directory on a specified machine.

## -parameters

### -param pMachineName

Reserved; must be **NULL**. This parameter is intended to point to the name of the machine on which the profile is to be installed. A **NULL** pointer indicates the local machine.

### -param pBuffer

Points to the buffer in which the color directory path is to be placed.

### -param pdwSize

Points to a variable containing the size in bytes of the buffer pointed to by *pBuffer*. On return, the variable contains the size of the buffer actually used or needed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

**Per-user/LUA support**

Color directory is still system-wide. This function is executable in LUA context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
