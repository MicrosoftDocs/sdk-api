---
UID: NS:powrprof._POWER_POLICY
title: POWER_POLICY (powrprof.h)
author: windows-sdk-content
description: Contains power policy settings that are unique to each power scheme.
old-location: base\power_policy_str.htm
tech.root: power
ms.assetid: ba49fca6-04b6-4627-a653-07c3fc0dab22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PPOWER_POLICY, POWER_POLICY, POWER_POLICY structure, PPOWER_POLICY, PPOWER_POLICY structure pointer, _win32_power_policy_str, base.power_policy_str, powrprof/POWER_POLICY, powrprof/PPOWER_POLICY'
ms.topic: struct
f1_keywords:
- powrprof/POWER_POLICY
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
- POWER_POLICY
product: Windows
targetos: Windows
req.typenames: POWER_POLICY, *PPOWER_POLICY
req.redist: 
ms.custom: 19H1
---

# POWER_POLICY structure


## -description


Contains power policy settings that are unique to each power scheme.


## -struct-fields




### -field user

A 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-user_power_policy">USER_POWER_POLICY</a> structure that defines user power policy settings.


### -field mach

A 
<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-machine_power_policy">MACHINE_POWER_POLICY</a> structure that defines computer power policy settings.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-enumpwrschemes">EnumPwrSchemes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-machine_power_policy">MACHINE_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-readpwrscheme">ReadPwrScheme</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/ns-powrprof-user_power_policy">USER_POWER_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>
 

 

