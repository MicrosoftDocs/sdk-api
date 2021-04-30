---
UID: NS:icm.tagPROFILE
title: PROFILE
description: Contains information that defines a color profile.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.typenames: PROFILE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - tagPROFILE
 - PROFILE
f1_keywords:
 - tagPROFILE
 - icm/tagPROFILE
 - PROFILE
 - icm/PROFILE
dev_langs:
 - c++
---

## -description

Contains information that defines a color profile. See [Using device profiles with WCS](/windows/win32/wcs/using-device-profiles-with-wcs) for more information.

## -struct-fields

### -field dwType

Must be set to one of the following values.

| Value              | Meaning                                                                                                                    |
|--------------------|----------------------------------------------------------------------------------------------------------------------------|
| PROFILE\_FILENAME  | Indicates that the **pProfileData** member contains a null-terminated string that holds the name of a device profile file. |
| PROFILE\_MEMBUFFER | Indicates that the **pProfileData** member contains a pointer to a device profile in a memory buffer.                      |

### -field pProfileData

The contents of this member is indicated by the **dwTYPE** member. It will either be a pointer to a null-terminated string containing the file name of the device profile, or it will be a pointer to a buffer in memory containing the device profile data.

### -field cbDataSize

The size in bytes of the data buffer pointed to by the **pProfileData** member.

## -remarks

## -see-also

* [Using device profiles with WCS](/windows/win32/wcs/using-device-profiles-with-wcs)
