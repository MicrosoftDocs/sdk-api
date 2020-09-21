---
UID: NS:powrprof._MACHINE_PROCESSOR_POWER_POLICY
title: MACHINE_PROCESSOR_POWER_POLICY (powrprof.h)
description: Contains processor power policy settings that apply while the system is running on AC power or battery power.
helpviewer_keywords: ["*PMACHINE_PROCESSOR_POWER_POLICY","MACHINE_PROCESSOR_POWER_POLICY","MACHINE_PROCESSOR_POWER_POLICY structure","PMACHINE_PROCESSOR_POWER_POLICY","PMACHINE_PROCESSOR_POWER_POLICY structure pointer","_win32_machine_processor_power_policy_str","base.machine_processor_power_policy_str","powrprof/MACHINE_PROCESSOR_POWER_POLICY","powrprof/PMACHINE_PROCESSOR_POWER_POLICY"]
old-location: base\machine_processor_power_policy_str.htm
tech.root: base
ms.assetid: 54403b81-97bc-4f2b-8721-48c9f69e2773
ms.date: 12/05/2018
ms.keywords: '*PMACHINE_PROCESSOR_POWER_POLICY, MACHINE_PROCESSOR_POWER_POLICY, MACHINE_PROCESSOR_POWER_POLICY structure, PMACHINE_PROCESSOR_POWER_POLICY, PMACHINE_PROCESSOR_POWER_POLICY structure pointer, _win32_machine_processor_power_policy_str, base.machine_processor_power_policy_str, powrprof/MACHINE_PROCESSOR_POWER_POLICY, powrprof/PMACHINE_PROCESSOR_POWER_POLICY'
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
req.typenames: MACHINE_PROCESSOR_POWER_POLICY, *PMACHINE_PROCESSOR_POWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MACHINE_PROCESSOR_POWER_POLICY
 - powrprof/_MACHINE_PROCESSOR_POWER_POLICY
 - PMACHINE_PROCESSOR_POWER_POLICY
 - powrprof/PMACHINE_PROCESSOR_POWER_POLICY
 - MACHINE_PROCESSOR_POWER_POLICY
 - powrprof/MACHINE_PROCESSOR_POWER_POLICY
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
 - MACHINE_PROCESSOR_POWER_POLICY
---

# MACHINE_PROCESSOR_POWER_POLICY structure


## -description

Contains processor power policy settings that apply while the system is running on AC power or battery power.

## -struct-fields

### -field Revision

The current structure revision level. Set this value by calling <a href="/windows/desktop/api/powrprof/nf-powrprof-readprocessorpwrscheme">ReadProcessorPwrScheme</a> before using a  <b>MACHINE_PROCESSOR_POWER_POLICY</b> structure to set power policy.

### -field ProcessorPolicyAc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-processor_power_policy">PROCESSOR_POWER_POLICY</a> structure that defines the processor power policy settings used while the computer is running on AC power.

### -field ProcessorPolicyDc

A 
<a href="/windows/desktop/api/winnt/ns-winnt-processor_power_policy">PROCESSOR_POWER_POLICY</a> structure that defines the processor power policy settings used while the computer is running on battery power.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-processor_power_policy">PROCESSOR_POWER_POLICY</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-readprocessorpwrscheme">ReadProcessorPwrScheme</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-writeprocessorpwrscheme">WriteProcessorPwrScheme</a>