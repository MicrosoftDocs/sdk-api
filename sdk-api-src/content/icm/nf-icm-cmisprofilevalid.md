---
UID: NF:icm.CMIsProfileValid
title: CMIsProfileValid
description: Reports whether the given profile is a valid ICC profile that can be used for color management.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
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
 - icm.h
api_name:
 - CMIsProfileValid
f1_keywords:
 - CMIsProfileValid
 - icm/CMIsProfileValid
dev_langs:
 - c++
---

## -description

Reports whether the given profile is a valid ICC profile that can be used for color management.

## -parameters

### -param hProfile

Specifies the profile to check.

### -param lpbValid

Pointer to a variable that is set on exit to TRUE if the profile is a valid ICC profile, or FALSE if not.

## -returns

If this function succeeds, the return value is TRUE.

If this function fails, the return value is FALSE. If the function fails, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

Only the Windows default CMM is required to export this function; it is optional for all other CMMs.

If a CMM does not support this function, Windows uses the default CMM to validate the profile.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
