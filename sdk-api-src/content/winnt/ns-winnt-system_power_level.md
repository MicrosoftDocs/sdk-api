---
UID: NS:winnt.SYSTEM_POWER_LEVEL
title: SYSTEM_POWER_LEVEL (winnt.h)
description: Contains information about system battery drain policy settings.
helpviewer_keywords: ["*PSYSTEM_POWER_LEVEL","PSYSTEM_POWER_LEVEL","PSYSTEM_POWER_LEVEL structure pointer","SYSTEM_POWER_LEVEL","SYSTEM_POWER_LEVEL structure","_win32_system_power_level_str","base.system_power_level_str","winnt/PSYSTEM_POWER_LEVEL","winnt/SYSTEM_POWER_LEVEL"]
old-location: base\system_power_level_str.htm
tech.root: base
ms.assetid: 4efa847d-92da-4cf7-95c2-c329de1691f4
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_POWER_LEVEL, PSYSTEM_POWER_LEVEL, PSYSTEM_POWER_LEVEL structure pointer, SYSTEM_POWER_LEVEL, SYSTEM_POWER_LEVEL structure, _win32_system_power_level_str, base.system_power_level_str, winnt/PSYSTEM_POWER_LEVEL, winnt/SYSTEM_POWER_LEVEL'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SYSTEM_POWER_LEVEL, *PSYSTEM_POWER_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSYSTEM_POWER_LEVEL
 - winnt/PSYSTEM_POWER_LEVEL
 - SYSTEM_POWER_LEVEL
 - winnt/SYSTEM_POWER_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_POWER_LEVEL
---

# SYSTEM_POWER_LEVEL structure


## -description

Contains information about system battery drain policy settings. This structure is part of the 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_user_power_policy">GLOBAL_USER_POWER_POLICY</a> structure.

## -struct-fields

### -field Enable

If this member is <b>TRUE</b>, the alarm should be activated when the battery discharges below the value set in <b>BatteryLevel</b>.

### -field Spare

Reserved.

### -field BatteryLevel

The battery capacity for this battery discharge policy, expressed as a percentage.

### -field PowerPolicy

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take for this battery discharge policy.

### -field MinSystemState

The minimum system sleep state to enter when the battery discharges below the value set in <b>BatteryLevel</b>. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values.

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-global_user_power_policy">GLOBAL_USER_POWER_POLICY</a>



<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a>

