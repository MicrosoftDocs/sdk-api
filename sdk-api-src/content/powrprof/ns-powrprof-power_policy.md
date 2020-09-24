---
UID: NS:powrprof._POWER_POLICY
title: POWER_POLICY (powrprof.h)
description: Contains power policy settings that are unique to each power scheme.
helpviewer_keywords: ["*PPOWER_POLICY","POWER_POLICY","POWER_POLICY structure","PPOWER_POLICY","PPOWER_POLICY structure pointer","_win32_power_policy_str","base.power_policy_str","powrprof/POWER_POLICY","powrprof/PPOWER_POLICY"]
old-location: base\power_policy_str.htm
tech.root: base
ms.assetid: ba49fca6-04b6-4627-a653-07c3fc0dab22
ms.date: 12/05/2018
ms.keywords: '*PPOWER_POLICY, POWER_POLICY, POWER_POLICY structure, PPOWER_POLICY, PPOWER_POLICY structure pointer, _win32_power_policy_str, base.power_policy_str, powrprof/POWER_POLICY, powrprof/PPOWER_POLICY'
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
req.typenames: POWER_POLICY, *PPOWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POWER_POLICY
 - powrprof/_POWER_POLICY
 - PPOWER_POLICY
 - powrprof/PPOWER_POLICY
 - POWER_POLICY
 - powrprof/POWER_POLICY
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
 - POWER_POLICY
---

# POWER_POLICY structure


## -description

Contains power policy settings that are unique to each power scheme.

## -struct-fields

### -field user

A 
<a href="/windows/desktop/api/powrprof/ns-powrprof-user_power_policy">USER_POWER_POLICY</a> structure that defines user power policy settings.

### -field mach

A 
<a href="/windows/desktop/api/powrprof/ns-powrprof-machine_power_policy">MACHINE_POWER_POLICY</a> structure that defines computer power policy settings.

## -see-also

<a href="/windows/desktop/api/powrprof/nf-powrprof-enumpwrschemes">EnumPwrSchemes</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-machine_power_policy">MACHINE_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-readpwrscheme">ReadPwrScheme</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a>



<a href="/windows/desktop/api/powrprof/ns-powrprof-user_power_policy">USER_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>