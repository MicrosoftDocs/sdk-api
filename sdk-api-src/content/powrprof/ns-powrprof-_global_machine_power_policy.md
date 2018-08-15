---
UID: NS:powrprof._GLOBAL_MACHINE_POWER_POLICY
title: "_GLOBAL_MACHINE_POWER_POLICY"
author: windows-sdk-content
description: Contains global computer power policy settings that apply to all power schemes for all users.
old-location: base\global_machine_power_policy_str.htm
old-project: power
ms.assetid: 79b57da4-0125-427b-aec7-7ca4c9bfb870
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PGLOBAL_MACHINE_POWER_POLICY, GLOBAL_MACHINE_POWER_POLICY, GLOBAL_MACHINE_POWER_POLICY structure, PGLOBAL_MACHINE_POWER_POLICY, PGLOBAL_MACHINE_POWER_POLICY structure pointer, _GLOBAL_MACHINE_POWER_POLICY, _win32_global_machine_power_policy_str, base.global_machine_power_policy_str, powrprof/GLOBAL_MACHINE_POWER_POLICY, powrprof/PGLOBAL_MACHINE_POWER_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: powrprof.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: GLOBAL_MACHINE_POWER_POLICY, *PGLOBAL_MACHINE_POWER_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PowrProf.h
api_name:
 - GLOBAL_MACHINE_POWER_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _GLOBAL_MACHINE_POWER_POLICY structure


## -description


Contains global computer power policy settings that apply to all power schemes for all 
   users. This structure is part of the 
   <a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a> structure.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling 
      <a href="https://msdn.microsoft.com/9a834fb6-35ae-4d36-885c-0d81cd39e9a6">GetCurrentPowerPolicies</a> or 
      <a href="https://msdn.microsoft.com/65da3d9f-b688-4d41-9da0-05159297d169">ReadGlobalPwrPolicy</a> before using a 
      <b>GLOBAL_MACHINE_POWER_POLICY</b> structure 
      to set power policy.


### -field LidOpenWakeAc

The maximum power state (highest Sx value) from which a lid-open event should wake the system when running 
      on AC power. This member must be one of the 
      <a href="https://msdn.microsoft.com/57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d">SYSTEM_POWER_STATE</a> enumeration type values. A value 
      of <b>PowerSystemUnspecified</b> indicates that a lid-open event does not wake the 
      system.


### -field LidOpenWakeDc

The maximum power state (highest Sx value) from which a lid-open event should wake the system when running 
      on battery. This member must be one of the 
      <a href="https://msdn.microsoft.com/57436a4b-0d18-4f7e-8dc0-fc5e68b44e7d">SYSTEM_POWER_STATE</a> enumeration type values. A value 
      of <b>PowerSystemUnspecified</b> indicates that a lid-open event does not wake the 
      system.


### -field BroadcastCapacityResolution

The resolution of change in the current battery capacity that should cause the system to be notified of a 
      system power state changed event.


## -see-also




<a href="https://msdn.microsoft.com/5c177093-0c16-4a84-9212-f2376de6965b">GLOBAL_POWER_POLICY</a>
 

 

