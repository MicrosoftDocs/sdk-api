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
 

 

