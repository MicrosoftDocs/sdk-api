---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

