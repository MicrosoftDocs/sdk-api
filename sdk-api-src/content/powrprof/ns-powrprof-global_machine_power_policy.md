---
UID: NS:powrprof._GLOBAL_MACHINE_POWER_POLICY
title: GLOBAL_MACHINE_POWER_POLICY (powrprof.h)
description: Contains global computer power policy settings that apply to all power schemes for all users.
old-location: base\global_machine_power_policy_str.htm
tech.root: power
ms.assetid: 79b57da4-0125-427b-aec7-7ca4c9bfb870
ms.date: 12/05/2018
ms.keywords: '*PGLOBAL_MACHINE_POWER_POLICY, GLOBAL_MACHINE_POWER_POLICY, GLOBAL_MACHINE_POWER_POLICY structure, PGLOBAL_MACHINE_POWER_POLICY, PGLOBAL_MACHINE_POWER_POLICY structure pointer, _win32_global_machine_power_policy_str, base.global_machine_power_policy_str, powrprof/GLOBAL_MACHINE_POWER_POLICY, powrprof/PGLOBAL_MACHINE_POWER_POLICY'
ms.topic: struct
f1_keywords:
- powrprof/GLOBAL_MACHINE_POWER_POLICY
dev_langs:
- c++
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
- GLOBAL_MACHINE_POWER_POLICY
targetos: Windows
req.typenames: GLOBAL_MACHINE_POWER_POLICY, *PGLOBAL_MACHINE_POWER_POLICY
req.redist: 
ms.custom: 19H1
---

# GLOBAL_MACHINE_POWER_POLICY structure


## -description


Contains global computer power policy settings that apply to all power schemes for all 
   users. This structure is part of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a> structure.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling 
      <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-getcurrentpowerpolicies">GetCurrentPowerPolicies</a> or 
      <a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-readglobalpwrpolicy">ReadGlobalPwrPolicy</a> before using a 
      <b>GLOBAL_MACHINE_POWER_POLICY</b> structure 
      to set power policy.


### -field LidOpenWakeAc

The maximum power state (highest Sx value) from which a lid-open event should wake the system when running 
      on AC power. This member must be one of the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values. A value 
      of <b>PowerSystemUnspecified</b> indicates that a lid-open event does not wake the 
      system.


### -field LidOpenWakeDc

The maximum power state (highest Sx value) from which a lid-open event should wake the system when running 
      on battery. This member must be one of the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-system_power_state">SYSTEM_POWER_STATE</a> enumeration type values. A value 
      of <b>PowerSystemUnspecified</b> indicates that a lid-open event does not wake the 
      system.


### -field BroadcastCapacityResolution

The resolution of change in the current battery capacity that should cause the system to be notified of a 
      system power state changed event.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-global_power_policy">GLOBAL_POWER_POLICY</a>
 

 

