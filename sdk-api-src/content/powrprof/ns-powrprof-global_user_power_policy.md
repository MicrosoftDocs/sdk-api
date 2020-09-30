---
UID: NS:powrprof._GLOBAL_USER_POWER_POLICY
title: GLOBAL_USER_POWER_POLICY (powrprof.h)
description: Contains global user power policy settings that apply to all power schemes for a user.
helpviewer_keywords: ["*PGLOBAL_USER_POWER_POLICY","GLOBAL_USER_POWER_POLICY","GLOBAL_USER_POWER_POLICY structure","PGLOBAL_USER_POWER_POLICY","PGLOBAL_USER_POWER_POLICY structure pointer","_win32_global_user_power_policy_str","base.global_user_power_policy_str","powrprof/GLOBAL_USER_POWER_POLICY","powrprof/PGLOBAL_USER_POWER_POLICY"]
old-location: base\global_user_power_policy_str.htm
tech.root: base
ms.assetid: 0e89ae66-a889-4929-b028-125fcef5c89c
ms.date: 12/05/2018
ms.keywords: '*PGLOBAL_USER_POWER_POLICY, GLOBAL_USER_POWER_POLICY, GLOBAL_USER_POWER_POLICY structure, PGLOBAL_USER_POWER_POLICY, PGLOBAL_USER_POWER_POLICY structure pointer, _win32_global_user_power_policy_str, base.global_user_power_policy_str, powrprof/GLOBAL_USER_POWER_POLICY, powrprof/PGLOBAL_USER_POWER_POLICY'
req.header: powrprof.h
req.include-header: 
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
req.typenames: GLOBAL_USER_POWER_POLICY, *PGLOBAL_USER_POWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GLOBAL_USER_POWER_POLICY
 - powrprof/_GLOBAL_USER_POWER_POLICY
 - PGLOBAL_USER_POWER_POLICY
 - powrprof/PGLOBAL_USER_POWER_POLICY
 - GLOBAL_USER_POWER_POLICY
 - powrprof/GLOBAL_USER_POWER_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PowrProf.h
api_name:
 - GLOBAL_USER_POWER_POLICY
---

# GLOBAL_USER_POWER_POLICY structure


## -description

Contains global user power policy settings that apply to all power schemes for a user. This structure is part of the 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure.

## -struct-fields

### -field Revision

The current structure revision level. Set this value by calling <a href="/windows/desktop/api/powrprof/nf-powrprof-getcurrentpowerpolicies">GetCurrentPowerPolicies</a> or  <a href="/windows/desktop/api/powrprof/nf-powrprof-readglobalpwrpolicy">ReadGlobalPwrPolicy</a> before using a <b>GLOBAL_USER_POWER_POLICY</b> structure to set power policy.

### -field PowerButtonAc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when the power button is pressed and the system is running on AC power.

### -field PowerButtonDc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when the power button is pressed and the system is running on battery power.

### -field SleepButtonAc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when the sleep button is pressed and the system is running on AC power.

### -field SleepButtonDc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when the sleep button is pressed and the system is running on battery power.

### -field LidCloseAc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when the lid is closed and the system is running on AC power.

### -field LidCloseDc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when the lid is closed and the system is running on battery power.

### -field DischargePolicy

An array of 
<a href="/windows/desktop/api/winnt/ns-winnt-system_power_level">SYSTEM_POWER_LEVEL</a> structures that defines the actions to take at system battery discharge events.

### -field GlobalFlags

A flag that enables or disables miscellaneous user power policy settings. This member can be one or more of the values described in 
<a href="/windows/desktop/Power/global-flags-constants">Global Flags Constants</a>.

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a>



<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_level">SYSTEM_POWER_LEVEL</a>