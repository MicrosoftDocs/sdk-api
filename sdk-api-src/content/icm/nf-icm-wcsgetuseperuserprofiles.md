---
UID: NF:icm.WcsGetUsePerUserProfiles
title: WcsGetUsePerUserProfiles
description: Determines whether the user chose to use a per-user profile association list for the specified device.
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
 - WcsGetUsePerUserProfiles
f1_keywords:
 - WcsGetUsePerUserProfiles
 - icm/WcsGetUsePerUserProfiles
dev_langs:
 - c++
---

## -description

Determines whether the user chose to use a per-user profile association list for the specified device.

## -parameters

### -param pDeviceName

A pointer to a string containing the user-friendly name of the device.

### -param dwDeviceClass

A flag value specifying the class of the device. This parameter must take one of the following values.

| Value          | Description                        |
|----------------|------------------------------------|
| CLASS\_MONITOR | Specifies a display device.        |
| CLASS\_PRINTER | Specifies a printer.               |
| CLASS\_SCANNER | Specifies an image-capture device. |

### -param pUsePerUserProfiles

A pointer to a location to receive a Boolean value that is **TRUE** if the user chose to use a per-user profile association list for the specified device; otherwise **FALSE**.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function fails if *pDeviceName* points to a device that is not of the class specified by *dwDeviceClass*.

This function is executable in Least-Privileged User Account (LUA) context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [Functions](/windows/win32/wcs/functions)
* [WcsSetUsePerUserProfiles](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)
