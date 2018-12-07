---
UID: NS:powrprof._GLOBAL_USER_POWER_POLICY
title: "_GLOBAL_USER_POWER_POLICY"
author: windows-sdk-content
description: Contains global user power policy settings that apply to all power schemes for a user.
old-location: base\global_user_power_policy_str.htm
tech.root: power
ms.assetid: 0e89ae66-a889-4929-b028-125fcef5c89c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PGLOBAL_USER_POWER_POLICY, GLOBAL_USER_POWER_POLICY, GLOBAL_USER_POWER_POLICY structure, PGLOBAL_USER_POWER_POLICY, PGLOBAL_USER_POWER_POLICY structure pointer, _GLOBAL_USER_POWER_POLICY, _win32_global_user_power_policy_str, base.global_user_power_policy_str, powrprof/GLOBAL_USER_POWER_POLICY, powrprof/PGLOBAL_USER_POWER_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PowrProf.h
api_name:
 - GLOBAL_USER_POWER_POLICY
product: Windows
targetos: Windows
req.typenames: GLOBAL_USER_POWER_POLICY, *PGLOBAL_USER_POWER_POLICY
req.redist: 
---

# _GLOBAL_USER_POWER_POLICY structure


## -description


Contains global user power policy settings that apply to all power schemes for a user. This structure is part of the 
<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling <a href="https://msdn.microsoft.com/9a834fb6-35ae-4d36-885c-0d81cd39e9a6">GetCurrentPowerPolicies</a> or  <a href="https://msdn.microsoft.com/65da3d9f-b688-4d41-9da0-05159297d169">ReadGlobalPwrPolicy</a> before using a <b>GLOBAL_USER_POWER_POLICY</b> structure to set power policy.


### -field PowerButtonAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the power button is pressed and the system is running on AC power.


### -field PowerButtonDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the power button is pressed and the system is running on battery power.


### -field SleepButtonAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the sleep button is pressed and the system is running on AC power.


### -field SleepButtonDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the sleep button is pressed and the system is running on battery power.


### -field LidCloseAc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the lid is closed and the system is running on AC power.


### -field LidCloseDc

A 
<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a> structure that defines the action to take when the lid is closed and the system is running on battery power.


### -field DischargePolicy

An array of 
<a href="https://msdn.microsoft.com/4efa847d-92da-4cf7-95c2-c329de1691f4">SYSTEM_POWER_LEVEL</a> structures that defines the actions to take at system battery discharge events.


### -field GlobalFlags

A flag that enables or disables miscellaneous user power policy settings. This member can be one or more of the values described in 
<a href="https://msdn.microsoft.com/d98190ef-f70e-4796-960e-ff32d2cf6f4f">Global Flags Constants</a>.


## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/70739f46-54be-4748-8993-ffee3b2a8b6c">POWER_ACTION_POLICY</a>



<a href="https://msdn.microsoft.com/4efa847d-92da-4cf7-95c2-c329de1691f4">SYSTEM_POWER_LEVEL</a>
 

 

