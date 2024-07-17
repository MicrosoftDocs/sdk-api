---
UID: NE:winnt._USER_ACTIVITY_PRESENCE
tech.root: base
title: USER_ACTIVITY_PRESENCE
ms.date: 01/23/2024
targetos: Windows
description: Specifies the presence of a user for the purposes of power management based on activity detected.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _USER_ACTIVITY_PRESENCE
 - PUSER_ACTIVITY_PRESENCE
 - USER_ACTIVITY_PRESENCE
f1_keywords:
 - _USER_ACTIVITY_PRESENCE
 - winnt/_USER_ACTIVITY_PRESENCE
 - PUSER_ACTIVITY_PRESENCE
 - winnt/PUSER_ACTIVITY_PRESENCE
 - USER_ACTIVITY_PRESENCE
 - winnt/USER_ACTIVITY_PRESENCE
dev_langs:
 - c++
helpviewer_keywords:
 - _USER_ACTIVITY_PRESENCE
---

# USER_ACTIVITY_PRESENCE enumeration

## -description

Specifies the presence of a user for the purposes of power management based on activity detected.

## -enum-fields

### -field PowerUserPresent

The user is present in a local or remote session on the system.

### -field PowerUserNotPresent

The user is not present in any local or remote session on the system.

### -field PowerUserInactive

The user is not active in any local or remote session on the system.

### -field PowerUserMaximum

PowerUserMaximum = PowerUserInvalid.

### -field PowerUserInvalid

Invalid state.

## -remarks

## -see-also

[Power Setting GUIDs](/windows/win32/power/power-setting-guids)
