---
UID: NF:icm.IsColorProfileValid
title: IsColorProfileValid
description: Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.
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
 - IsColorProfileValid
f1_keywords:
 - IsColorProfileValid
 - icm/IsColorProfileValid
dev_langs:
 - c++
---

## -description

Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management. WCS profile validation doesn't invoke the underlying device models, but instead simply validates against the XML schema and the schema element range limits.

## -parameters

### -param hProfile

Specifies a handle to the profile to be validated. The function determines whether the HPROFILE contains ICC or WCS profile information.

### -param pbValid

Pointer to a variable that is set to **TRUE** on return if the operation succeeds and the profile is a valid ICC or WCS profile. If the operation fails or the profile is not valid the variable is **FALSE**.

## -returns

If this function succeeds and the profile is valid, the return value is **TRUE**.

If this function fails (or succeeds and the profile is not valid), the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
