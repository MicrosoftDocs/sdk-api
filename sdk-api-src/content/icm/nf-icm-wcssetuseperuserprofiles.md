---
UID: NF:icm.WcsSetUsePerUserProfiles
title: WcsSetUsePerUserProfiles
description: Enables a user to specify whether or not to use a per-user profile association list for the specified device.
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
 - WcsSetUsePerUserProfiles
f1_keywords:
 - WcsSetUsePerUserProfiles
 - icm/WcsSetUsePerUserProfiles
dev_langs:
 - c++
---

## -description

Enables a user to specify whether or not to use a per-user profile association list for the specified device.

## -parameters

### -param pDeviceName

A pointer to a string that contains the user-friendly name of the device.

### -param dwDeviceClass

A flag value that specifies the class of the device. This parameter must take one of the following values:

|  Value         |   Description                      |
|----------------|------------------------------------|
| CLASS\_MONITOR | Specifies a display device.        |
| CLASS\_PRINTER | Specifies a printer.               |
| CLASS\_SCANNER | Specifies an image capture device. |

### -param usePerUserProfiles

A Boolean value that is **TRUE** if the user wants to use a per-user profile association list for the specified device; otherwise **FALSE**.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If *usePerUserProfiles* is **TRUE**, and the user is not already using a per-user profile association list for *pDeviceName*, then the per-user profile association list is initialized by making a copy of the system-wide profile association list for the same device. From then on, changes to the system-wide list are not included in the per-user list.

This function is executable in Least-Privileged User Account (LUA) context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [Functions](/windows/win32/wcs/functions)
* [WcsGetUsePerUserProfiles](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)
