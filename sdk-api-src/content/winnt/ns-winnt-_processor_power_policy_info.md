---
UID: NS:winnt._PROCESSOR_POWER_POLICY_INFO
title: "_PROCESSOR_POWER_POLICY_INFO"
author: windows-sdk-content
description: Contains information about processor C-state policy settings.
old-location: base\processor_power_policy_info_str.htm
old-project: power
ms.assetid: 9d29aec0-ba22-46be-b429-d6dfd2191b98
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: "*PPROCESSOR_POWER_POLICY_INFO, PPROCESSOR_POWER_POLICY_INFO, PPROCESSOR_POWER_POLICY_INFO structure pointer, PROCESSOR_POWER_POLICY_INFO, PROCESSOR_POWER_POLICY_INFO structure, _PROCESSOR_POWER_POLICY_INFO, _win32_processor_power_policy_info_str, base.processor_power_policy_info_str, winnt/PPROCESSOR_POWER_POLICY_INFO, winnt/PROCESSOR_POWER_POLICY_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROCESSOR_POWER_POLICY_INFO, *PPROCESSOR_POWER_POLICY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESSOR_POWER_POLICY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PROCESSOR_POWER_POLICY_INFO structure


## -description


Contains information about processor C-state policy settings. This structure is part of the 
<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a> structure.


## -struct-fields




### -field TimeCheck

The time that must expire before promotion or demotion is considered, in microseconds.


### -field DemoteLimit

The minimum amount of time that must be spent in the idle loop to avoid demotion, in microseconds.


### -field PromoteLimit

The time that must be exceeded to cause promotion to a deeper idle state, in microseconds.


### -field DemotePercent

The value that scales the threshold at which the power policy manager decreases the performance of the processor, expressed as a percentage.


### -field PromotePercent

The value that scales the threshold at which the power policy manager increases the performance of the processor, expressed as a percentage.


### -field Spare

Reserved.


### -field AllowDemotion

When set, allows the kernel power policy manager to demote from the current state.


### -field AllowPromotion

When set, allows the kernel power policy manager to promote from the current state.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a>
 

 

