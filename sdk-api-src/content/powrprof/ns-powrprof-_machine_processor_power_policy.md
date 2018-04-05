---
UID: NS:powrprof._MACHINE_PROCESSOR_POWER_POLICY
title: "_MACHINE_PROCESSOR_POWER_POLICY"
author: windows-driver-content
description: Contains processor power policy settings that apply while the system is running on AC power or battery power.
old-location: base\machine_processor_power_policy_str.htm
old-project: Power
ms.assetid: 54403b81-97bc-4f2b-8721-48c9f69e2773
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PMACHINE_PROCESSOR_POWER_POLICY, MACHINE_PROCESSOR_POWER_POLICY, MACHINE_PROCESSOR_POWER_POLICY structure, PMACHINE_PROCESSOR_POWER_POLICY, PMACHINE_PROCESSOR_POWER_POLICY structure pointer, _MACHINE_PROCESSOR_POWER_POLICY, _win32_machine_processor_power_policy_str, base.machine_processor_power_policy_str, powrprof/MACHINE_PROCESSOR_POWER_POLICY, powrprof/PMACHINE_PROCESSOR_POWER_POLICY"
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
req.typenames: MACHINE_PROCESSOR_POWER_POLICY, *PMACHINE_PROCESSOR_POWER_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PowrProf.h
api_name:
-	MACHINE_PROCESSOR_POWER_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _MACHINE_PROCESSOR_POWER_POLICY structure


## -description


Contains processor power policy settings that apply while the system is running on AC power or battery power.


## -struct-fields




### -field Revision

The current structure revision level. Set this value by calling <a href="https://msdn.microsoft.com/740095a7-9def-48a3-9cbb-1da91b052321">ReadProcessorPwrScheme</a> before using a  <b>MACHINE_PROCESSOR_POWER_POLICY</b> structure to set power policy.


### -field ProcessorPolicyAc

A 
<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a> structure that defines the processor power policy settings used while the computer is running on AC power.


### -field ProcessorPolicyDc

A 
<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a> structure that defines the processor power policy settings used while the computer is running on battery power.


## -see-also




<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/740095a7-9def-48a3-9cbb-1da91b052321">ReadProcessorPwrScheme</a>



<a href="https://msdn.microsoft.com/70e18f50-4774-4a7c-8fe0-7fd6a54aaa90">WriteProcessorPwrScheme</a>
 

 

