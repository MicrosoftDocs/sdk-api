---
UID: NS:winnt._SYSTEM_POWER_POLICY
title: SYSTEM_POWER_POLICY (winnt.h)
description: Contains information about the current system power policy.
helpviewer_keywords: ["*PSYSTEM_POWER_POLICY","PSYSTEM_POWER_POLICY","PSYSTEM_POWER_POLICY structure pointer","SYSTEM_POWER_POLICY","SYSTEM_POWER_POLICY structure","_SYSTEM_POWER_POLICY","_win32_system_power_policy_str","base.system_power_policy_str","winnt/PSYSTEM_POWER_POLICY","winnt/SYSTEM_POWER_POLICY"]
old-location: base\system_power_policy_str.htm
tech.root: base
ms.assetid: 0e73e94d-e529-46fb-b3e5-a79ba2c05713
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_POWER_POLICY, PSYSTEM_POWER_POLICY, PSYSTEM_POWER_POLICY structure pointer, SYSTEM_POWER_POLICY, SYSTEM_POWER_POLICY structure, _SYSTEM_POWER_POLICY, _win32_system_power_policy_str, base.system_power_policy_str, winnt/PSYSTEM_POWER_POLICY, winnt/SYSTEM_POWER_POLICY'
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
req.typenames: SYSTEM_POWER_POLICY, *PSYSTEM_POWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_POWER_POLICY
 - winnt/_SYSTEM_POWER_POLICY
 - PSYSTEM_POWER_POLICY
 - winnt/PSYSTEM_POWER_POLICY
 - SYSTEM_POWER_POLICY
 - winnt/SYSTEM_POWER_POLICY
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
 - SYSTEM_POWER_POLICY
---

# SYSTEM_POWER_POLICY structure


## -description

Contains information about the current system power policy.

## -struct-fields

### -field Revision

The current structure revision.

### -field PowerButton

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate when the system power button is pressed.

### -field SleepButton

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate when the system sleep button is pressed.

### -field LidClose

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate when the system lid switch is closed.

### -field LidOpenWake

The maximum power state (highest Sx value) from which a lid-open event should wake the system. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values.

### -field Reserved

Reserved.

### -field Idle

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate when the system idle timer expires.

### -field IdleTimeout

The time that the level of system activity must remain below the idle detection threshold before the system idle timer expires, in seconds.

### -field IdleSensitivity

The level of system activity that defines the threshold for idle detection, expressed as a percentage.

### -field DynamicThrottle

The current system processor dynamic throttling policy. This member must be one of the values described in 
<a href="/windows/desktop/Power/processor-performance-control-policy-constants">Processor Performance Control Policy Constants</a>.

### -field Spare2

Reserved.

### -field MinSleep

The minimum system sleep state (lowest Sx value) currently supported. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values.

### -field MaxSleep

The maximum system sleep state (highest Sx value) currently supported. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values.

### -field ReducedLatencySleep

The system power state (Sx value) to enter on a system sleep action when there are outstanding latency requirements. This member must be one of the 
<a href="/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values. If an application calls 
<a href="/windows/desktop/api/winbase/nf-winbase-requestwakeuplatency">RequestWakeupLatency</a> with LT_LOWEST_LATENCY, <b>ReducedLatencySleep</b> will be used in place of <b>MaxSleep</b>.

### -field WinLogonFlags

This member can be zero or WINLOGON_LOCK_ON_SLEEP (0x00000001).

### -field Spare3

Reserved.

### -field DozeS4Timeout

The time to wait between entering the suspend state and entering the hibernate sleeping state, in seconds. A value of zero indicates never hibernate.

### -field BroadcastCapacityResolution

The resolution of change in current battery capacity that should cause the system to be notified of a system power state changed event.

### -field DischargePolicy

An array of 
<a href="/windows/desktop/api/winnt/ns-winnt-system_power_level">SYSTEM_POWER_LEVEL</a> structures that defines the actions to take at system battery discharge events.

### -field VideoTimeout

The time before the display is turned off, in seconds.

### -field VideoDimDisplay

If this member is <b>TRUE</b>, the system includes support for display dimming.

### -field VideoReserved

Reserved.

### -field SpindownTimeout

The time before power to fixed disk drives is turned off, in seconds.

### -field OptimizeForPower

If this member is <b>TRUE</b>, the system will turn on cooling fans and run the processor at full speed when passive cooling is specified. This causes the operating system to be biased toward using the fan and running the processor at full speed.

### -field FanThrottleTolerance

The lower limit that the processor may be throttled down to prior to turning on system fans in response to a thermal event, expressed as a percentage.

### -field ForcedThrottle

The processor throttle level to be imposed by the system, expressed as a percentage.

### -field MinThrottle

The minimum processor throttle level, expressed as a percentage.

### -field OverThrottled

A 
<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate in response to a thermal event when processor throttling is unable to adequately reduce the system temperature.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-power_action_policy">POWER_ACTION_POLICY</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_level">SYSTEM_POWER_LEVEL</a>