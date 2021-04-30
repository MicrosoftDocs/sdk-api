---
UID: NS:powrprof._GLOBAL_POWER_POLICY
title: GLOBAL_POWER_POLICY (powrprof.h)
description: Contains global power policy settings that apply to all power schemes.
helpviewer_keywords: ["*PGLOBAL_POWER_POLICY","GLOBAL_POWER_POLICY","GLOBAL_POWER_POLICY structure","PGLOBAL_POWER_POLICY","PGLOBAL_POWER_POLICY structure pointer","_win32_global_power_policy_str","base.global_power_policy_str","powrprof/GLOBAL_POWER_POLICY","powrprof/PGLOBAL_POWER_POLICY"]
old-location: base\global_power_policy_str.htm
tech.root: base
ms.assetid: 5c177093-0c16-4a84-9212-f2376de6965b
ms.date: 12/05/2018
ms.keywords: '*PGLOBAL_POWER_POLICY, GLOBAL_POWER_POLICY, GLOBAL_POWER_POLICY structure, PGLOBAL_POWER_POLICY, PGLOBAL_POWER_POLICY structure pointer, _win32_global_power_policy_str, base.global_power_policy_str, powrprof/GLOBAL_POWER_POLICY, powrprof/PGLOBAL_POWER_POLICY'
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
req.typenames: GLOBAL_POWER_POLICY, *PGLOBAL_POWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GLOBAL_POWER_POLICY
 - powrprof/_GLOBAL_POWER_POLICY
 - PGLOBAL_POWER_POLICY
 - powrprof/PGLOBAL_POWER_POLICY
 - GLOBAL_POWER_POLICY
 - powrprof/GLOBAL_POWER_POLICY
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
 - GLOBAL_POWER_POLICY
---

# GLOBAL_POWER_POLICY structure


## -description

Contains global power policy settings that apply to all power schemes.

## -struct-fields

### -field user

A 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_user_power_policy">GLOBAL_USER_POWER_POLICY</a> structure that defines the global user power policy settings.

### -field mach

A 
<a href="/windows/desktop/api/powrprof/ns-powrprof-global_machine_power_policy">GLOBAL_MACHINE_POWER_POLICY</a> structure that defines the global computer power policy settings.

## -see-also

<a href="/windows/desktop/api/powrprof/ns-powrprof-global_machine_power_policy">GLOBAL_MACHINE_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-global_user_power_policy">GLOBAL_USER_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-getcurrentpowerpolicies">GetCurrentPowerPolicies</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-readglobalpwrpolicy">ReadGlobalPwrPolicy</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-writeglobalpwrpolicy">WriteGlobalPwrPolicy</a>