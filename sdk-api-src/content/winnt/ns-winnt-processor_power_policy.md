---
UID: NS:winnt._PROCESSOR_POWER_POLICY
title: PROCESSOR_POWER_POLICY (winnt.h)
description: Contains information about processor performance control and C-states.
helpviewer_keywords: ["*PPROCESSOR_POWER_POLICY","PPROCESSOR_POWER_POLICY","PPROCESSOR_POWER_POLICY structure pointer","PROCESSOR_POWER_POLICY","PROCESSOR_POWER_POLICY structure","_PROCESSOR_POWER_POLICY","_win32_processor_power_policy_str","base.processor_power_policy_str","winnt/PPROCESSOR_POWER_POLICY","winnt/PROCESSOR_POWER_POLICY"]
old-location: base\processor_power_policy_str.htm
tech.root: base
ms.assetid: ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a
ms.date: 12/05/2018
ms.keywords: '*PPROCESSOR_POWER_POLICY, PPROCESSOR_POWER_POLICY, PPROCESSOR_POWER_POLICY structure pointer, PROCESSOR_POWER_POLICY, PROCESSOR_POWER_POLICY structure, _PROCESSOR_POWER_POLICY, _win32_processor_power_policy_str, base.processor_power_policy_str, winnt/PPROCESSOR_POWER_POLICY, winnt/PROCESSOR_POWER_POLICY'
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
req.typenames: PROCESSOR_POWER_POLICY, *PPROCESSOR_POWER_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESSOR_POWER_POLICY
 - winnt/_PROCESSOR_POWER_POLICY
 - PPROCESSOR_POWER_POLICY
 - winnt/PPROCESSOR_POWER_POLICY
 - PROCESSOR_POWER_POLICY
 - winnt/PROCESSOR_POWER_POLICY
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
 - PROCESSOR_POWER_POLICY
---

# PROCESSOR_POWER_POLICY structure


## -description

Contains information about processor performance control and C-states.

## -struct-fields

### -field Revision

The current structure revision level.  Set this value by calling <a href="/windows/desktop/api/powrprof/nf-powrprof-readprocessorpwrscheme">ReadProcessorPwrScheme</a> before using a  <b>PROCESSOR_POWER_POLICY</b> structure to set power policy.

### -field DynamicThrottle

The current processor performance state policy. This member must be one of the values described in 
<a href="/windows/desktop/Power/processor-performance-control-policy-constants">Processor Performance Control Policy Constants</a>.

### -field Spare

Reserved; set to zero.

### -field DisableCStates

Reserved; set to zero.

### -field Reserved

Reserved; set to zero.

### -field PolicyCount

The number of elements in the <b>Policy</b> array.

### -field Policy

An array of 
<a href="/windows/desktop/api/winnt/ns-winnt-processor_power_policy_info">PROCESSOR_POWER_POLICY_INFO</a> structures that defines values used to apply processor C-state policy settings. Policy[0] corresponds to ACPI C-state C1, Policy[1] corresponds to C2, and Policy[2] corresponds to C3. The <b>AllowPromotion</b> member determines whether the processor can be promoted to the state. For example, if Policy[0].AllowPromotion is 0, the computer cannot transition from C0 to C1.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-callntpowerinformation">CallNtPowerInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-processor_power_policy_info">PROCESSOR_POWER_POLICY_INFO</a>