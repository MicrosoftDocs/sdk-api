---
UID: NS:powrprof._POWER_POLICY
title: "_POWER_POLICY"
author: windows-driver-content
description: Contains power policy settings that are unique to each power scheme.
old-location: base\power_policy_str.htm
old-project: Power
ms.assetid: ba49fca6-04b6-4627-a653-07c3fc0dab22
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PPOWER_POLICY, POWER_POLICY, POWER_POLICY structure, PPOWER_POLICY, PPOWER_POLICY structure pointer, _POWER_POLICY, _win32_power_policy_str, base.power_policy_str, powrprof/POWER_POLICY, powrprof/PPOWER_POLICY"
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
req.typenames: POWER_POLICY, *PPOWER_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PowrProf.h
api_name:
-	POWER_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _POWER_POLICY structure


## -description


Contains power policy settings that are unique to each power scheme.


## -struct-fields




### -field user

A 
<a href="https://msdn.microsoft.com/616c45f6-ec80-42d9-a485-e9e778f2b971">USER_POWER_POLICY</a> structure that defines user power policy settings.


### -field mach

A 
<a href="https://msdn.microsoft.com/41dca573-a73d-430c-9bd3-083e72aecbdc">MACHINE_POWER_POLICY</a> structure that defines computer power policy settings.


## -see-also




<a href="https://msdn.microsoft.com/5e9e10b4-84c3-40ec-8de9-220d13795403">EnumPwrSchemes</a>



<a href="https://msdn.microsoft.com/41dca573-a73d-430c-9bd3-083e72aecbdc">MACHINE_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/a8d93820-b652-4358-8039-8987fac95dca">ReadPwrScheme</a>



<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a>



<a href="https://msdn.microsoft.com/616c45f6-ec80-42d9-a485-e9e778f2b971">USER_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/b9233601-6848-41c4-bb58-27decad60ba5">WritePwrScheme</a>
 

 

