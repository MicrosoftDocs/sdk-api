---
UID: NS:powrprof._USER_POWER_POLICY
title: "_USER_POWER_POLICY"
author: windows-sdk-content
description: Contains power policy settings that are unique to each power scheme for a user.
old-location: base\user_power_policy_str.htm
old-project: Power
ms.assetid: 616c45f6-ec80-42d9-a485-e9e778f2b971
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: "*PUSER_POWER_POLICY, PUSER_POWER_POLICY, PUSER_POWER_POLICY structure pointer, USER_POWER_POLICY, USER_POWER_POLICY structure, _USER_POWER_POLICY, _win32_user_power_policy_str, base.user_power_policy_str, powrprof/PUSER_POWER_POLICY, powrprof/USER_POWER_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: USER_POWER_POLICY, *PUSER_POWER_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PowrProf.h
api_name:
-	USER_POWER_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _USER_POWER_POLICY structure


## -description


Contains power policy settings that are unique to each power scheme for a user. This structure is part of the 
<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a> structure.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling <a href="https://msdn.microsoft.com/9a834fb6-35ae-4d36-885c-0d81cd39e9a6">GetCurrentPowerPolicies</a> or  <a href="https://msdn.microsoft.com/a8d93820-b652-4358-8039-8987fac95dca">ReadPwrScheme</a> before using a <b>USER_POWER_POLICY</b> structure to set power policy.


### -field IdleAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate when the system is running on AC (utility) power and the system idle timer expires.


### -field IdleDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the system power action to initiate when the system is running on battery power and the system idle timer expires.


### -field IdleTimeoutAc

The time that the level of system activity must remain below the idle detection threshold before the system idle timer expires when running on AC (utility) power, in seconds.

This member is ignored if the system is performing an automated resume because there is no user present. To temporarily keep the system running while an application is performing a task, use the <a href="https://msdn.microsoft.com/9214ea84-7636-4a78-91fd-a5a5da8199a1">SetThreadExecutionState</a> function.


### -field IdleTimeoutDc

The time that the level of system activity must remain below the idle detection threshold before the system idle timer expires when running on battery power, in seconds.

This member is ignored if the system is performing an automated resume because there is no user present. To temporarily keep the system running while an application is performing a task, use the <a href="https://msdn.microsoft.com/9214ea84-7636-4a78-91fd-a5a5da8199a1">SetThreadExecutionState</a> function.


### -field IdleSensitivityAc

The level of system activity that defines the threshold for idle detection when the system is running on AC (utility) power, expressed as a percentage.


### -field IdleSensitivityDc

The level of system activity that defines the threshold for idle detection when the system is running on battery power, expressed as a percentage.


### -field ThrottlePolicyAc

The processor dynamic throttling policy to use when the system is running on AC (utility) power.


### -field ThrottlePolicyDc

The processor dynamic throttling policy to use when the system is running on battery power.


### -field MaxSleepAc

The maximum system sleep state when the system is running on AC (utility) power. This member must be one of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564565">SYSTEM_POWER_STATE</a> enumeration type values.


### -field MaxSleepDc

The maximum system sleep state when the system is running on battery power. This member must be one of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564565">SYSTEM_POWER_STATE</a> enumeration type values.


### -field Reserved

Reserved.


### -field VideoTimeoutAc

The time before the display is turned off when the system is running on AC (utility) power, in seconds.


### -field VideoTimeoutDc

The time before the display is turned off when the system is running on battery power, in seconds.


### -field SpindownTimeoutAc

The time before power to fixed disk drives is turned off when the system is running on AC (utility) power, in seconds.


### -field SpindownTimeoutDc

The time before power to fixed disk drives is turned off when the system is running on battery power, in seconds.


### -field OptimizeForPowerAc

If this member is <b>TRUE</b>, the system will turn on cooling fans and run the processor at full speed when passive cooling is specified and the system is running on AC (utility) power. This causes the operating system to be biased toward using the fan and running the processor at full speed.


### -field OptimizeForPowerDc

If this member is <b>TRUE</b>, the system will turn on cooling fans and run the processor at full speed when passive cooling is specified and the system is running on battery power. This causes the operating system to be biased toward using the fan and running the processor at full speed.


### -field FanThrottleToleranceAc

The lower limit that the processor may be throttled down to prior to turning on system fans in response to a thermal event while the system is operating on AC (utility) power, expressed as a percentage.


### -field FanThrottleToleranceDc

The lower limit that the processor may be throttled down to prior to turning on system fans in response to a thermal event while the system is operating on battery power, expressed as a percentage.


### -field ForcedThrottleAc

The processor throttle level to be imposed by the system while the computer is running on AC (utility) power, expressed as a percentage.


### -field ForcedThrottleDc

The processor throttle level to be imposed by the system while the computer is running on battery power, expressed as a percentage.


## -see-also




<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a>



<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a>
 

 

