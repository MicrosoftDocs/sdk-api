---
UID: NS:powrprof._MACHINE_POWER_POLICY
title: MACHINE_POWER_POLICY (powrprof.h)
description: Contains computer power policy settings that are unique to each power scheme on the computer.
helpviewer_keywords: ["*PMACHINE_POWER_POLICY","MACHINE_POWER_POLICY","MACHINE_POWER_POLICY structure","PMACHINE_POWER_POLICY","PMACHINE_POWER_POLICY structure pointer","_win32_machine_power_policy_str","base.machine_power_policy_str","powrprof/MACHINE_POWER_POLICY","powrprof/PMACHINE_POWER_POLICY"]
old-location: base\machine_power_policy_str.htm
tech.root: base
ms.assetid: 41dca573-a73d-430c-9bd3-083e72aecbdc
ms.date: 12/05/2018
ms.keywords: '*PMACHINE_POWER_POLICY, MACHINE_POWER_POLICY, MACHINE_POWER_POLICY structure, PMACHINE_POWER_POLICY, PMACHINE_POWER_POLICY structure pointer, _win32_machine_power_policy_str, base.machine_power_policy_str, powrprof/MACHINE_POWER_POLICY, powrprof/PMACHINE_POWER_POLICY'
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
req.typenames: MACHINE_POWER_POLICY, *PMACHINE_POWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MACHINE_POWER_POLICY
 - powrprof/_MACHINE_POWER_POLICY
 - PMACHINE_POWER_POLICY
 - powrprof/PMACHINE_POWER_POLICY
 - MACHINE_POWER_POLICY
 - powrprof/MACHINE_POWER_POLICY
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
 - MACHINE_POWER_POLICY
---

# MACHINE_POWER_POLICY structure


## -description

Contains computer power policy settings that are unique to each power scheme on the computer. This structure is part of the 
<a href="/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a> structure.

## -struct-fields

### -field Revision

The current structure revision level. Set this value by calling <a href="/windows/desktop/api/powrprof/nf-powrprof-getcurrentpowerpolicies">GetCurrentPowerPolicies</a> or  <a href="/windows/desktop/api/powrprof/nf-powrprof-readpwrscheme">ReadPwrScheme</a> before using a <b>MACHINE_POWER_POLICY</b> structure to set power policy.

### -field MinSleepAc

The minimum system power state (lowest Sx value) to enter on a system sleep action when running on AC power. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values.

### -field MinSleepDc

The minimum system power state (lowest Sx value) to enter on a system sleep action when running on battery power. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values.

### -field ReducedLatencySleepAc

The maximum system power state (highest Sx value) to enter on a system sleep action when running on AC power, and when there are outstanding latency requirements. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values. If an application calls 
<a href="/windows/desktop/api/winbase/nf-winbase-requestwakeuplatency">RequestWakeupLatency</a> with LT_LOWEST_LATENCY, <b>ReducedLatencySleepAc</b> is used in place of <b>MaxSleepAc</b>.

### -field ReducedLatencySleepDc

The maximum system power state (highest Sx value) to enter on a system sleep action when running on battery power, and when there are outstanding latency requirements. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values. If an application calls 
<a href="/windows/desktop/api/winbase/nf-winbase-requestwakeuplatency">RequestWakeupLatency</a> with LT_LOWEST_LATENCY, <b>ReducedLatencySleepAc</b> is used in place of <b>MaxSleepAc</b>.

### -field DozeTimeoutAc

This member is ignored.

### -field DozeTimeoutDc

This member is ignored.

### -field DozeS4TimeoutAc

Time to wait between entering the suspend state and entering the hibernate sleeping state when the system is running on AC power, in seconds. A value of zero indicates never hibernate.

### -field DozeS4TimeoutDc

Time to wait between entering the suspend state and entering the hibernate sleeping state when the system is running on battery power, in seconds. A value of zero indicates never hibernate.

### -field MinThrottleAc

The minimum throttle setting allowed before being overthrottled when the system is running on AC power. Thermal conditions would be the only reason for going below the minimum setting. When the processor is overthrottled, the system will initiate the <b>OverThrottledAc</b> policy. Note that the power policy manager has a hard-coded policy to initiate a CriticalShutdownOff whenever any thermal zone indicates a critical thermal condition. Range: 0-100.

### -field MinThrottleDc

The minimum throttle setting allowed before being overthrottled when the system is running on battery power. Thermal conditions would be the only reason for going below the minimum setting. When the processor is overthrottled, the system will initiate the <b>OverThrottledDc</b> policy. Note that the power policy manager has a hard-coded policy to initiate a CriticalShutdownOff whenever any thermal zone indicates a critical thermal condition. Range: 0-100.

### -field pad1

Reserved.

### -field OverThrottledAc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when a processor has become overthrottled (as defined by the <b>MinThrottleAc</b> member) when the system is running on AC power.

### -field OverThrottledDc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the action to take when a processor has become overthrottled (as defined by the <b>MinThrottleDc</b> member) when the system is running on battery power.

## -remarks

<b>DozeS4TimeoutAc</b> and <b>DozeS4TimeoutDc</b>  correspond to the <b>DozeS4Timeout</b> member of <a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a>. These values are merged from the machine power policy to the system power policy when the <a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a> function is called to apply a power scheme.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-power_policy">POWER_POLICY</a>