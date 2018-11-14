---
UID: NS:winnt._PROCESSOR_POWER_POLICY
title: "_PROCESSOR_POWER_POLICY"
author: windows-sdk-content
description: Contains information about processor performance control and C-states.
old-location: base\processor_power_policy_str.htm
tech.root: power
ms.assetid: ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PPROCESSOR_POWER_POLICY, PPROCESSOR_POWER_POLICY, PPROCESSOR_POWER_POLICY structure pointer, PROCESSOR_POWER_POLICY, PROCESSOR_POWER_POLICY structure, _PROCESSOR_POWER_POLICY, _win32_processor_power_policy_str, base.processor_power_policy_str, winnt/PPROCESSOR_POWER_POLICY, winnt/PROCESSOR_POWER_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESSOR_POWER_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESSOR_POWER_POLICY, *PPROCESSOR_POWER_POLICY
req.redist: 
---

# _PROCESSOR_POWER_POLICY structure


## -description


Contains information about processor performance control and C-states.


## -struct-fields




### -field Revision

The current structure revision level.  Set this value by calling <a href="https://msdn.microsoft.com/740095a7-9def-48a3-9cbb-1da91b052321">ReadProcessorPwrScheme</a> before using a  <b>PROCESSOR_POWER_POLICY</b> structure to set power policy.


### -field DynamicThrottle

The current processor performance state policy. This member must be one of the values described in 
<a href="https://msdn.microsoft.com/928ba485-f767-47df-8b57-7630c68068a7">Processor Performance Control Policy Constants</a>.


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
<a href="https://msdn.microsoft.com/9d29aec0-ba22-46be-b429-d6dfd2191b98">PROCESSOR_POWER_POLICY_INFO</a> structures that defines values used to apply processor C-state policy settings. Policy[0] corresponds to ACPI C-state C1, Policy[1] corresponds to C2, and Policy[2] corresponds to C3. The <b>AllowPromotion</b> member determines whether the processor can be promoted to the state. For example, if Policy[0].AllowPromotion is 0, the computer cannot transition from C0 to C1.


## -see-also




<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a>



<a href="https://msdn.microsoft.com/9d29aec0-ba22-46be-b429-d6dfd2191b98">PROCESSOR_POWER_POLICY_INFO</a>
 

 

