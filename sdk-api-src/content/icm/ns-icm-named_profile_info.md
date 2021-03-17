---
UID: NS:icm.tagNAMED_PROFILE_INFO
title: NAMED_PROFILE_INFO
description: The **NAMED_PROFILE_INFO** structure is used to store information about a named color profile.
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
req.typenames: NAMED_PROFILE_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - tagNAMED_PROFILE_INFO
 - NAMED_PROFILE_INFO
f1_keywords:
 - tagNAMED_PROFILE_INFO
 - icm/tagNAMED_PROFILE_INFO
 - NAMED_PROFILE_INFO
 - icm/NAMED_PROFILE_INFO
dev_langs:
 - c++
---

## -description

The **NAMED_PROFILE_INFO** structure is used to store information about a named color profile.

## -struct-fields

### -field dwFlags

Not currently used by the default CMM.

### -field dwCount

Total number of named colors in the profile.

### -field dwCountDevCoordinates

Total number of device coordinates for each named color.

### -field szPrefix

Pointer to a string containing the prefix for each color name.

### -field szSuffix

Pointer to a string containing the suffix for each color name.

## -remarks

## -see-also
