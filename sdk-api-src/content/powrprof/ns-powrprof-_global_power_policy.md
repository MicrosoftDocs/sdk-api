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

# _GLOBAL_POWER_POLICY structure


## -description


Contains global power policy settings that apply to all power schemes.


## -struct-fields




### -field user

A 
<a href="https://msdn.microsoft.com/0e89ae66-a889-4929-b028-125fcef5c89c">GLOBAL_USER_POWER_POLICY</a> structure that defines the global user power policy settings.


### -field mach

A 
<a href="https://msdn.microsoft.com/79b57da4-0125-427b-aec7-7ca4c9bfb870">GLOBAL_MACHINE_POWER_POLICY</a> structure that defines the global computer power policy settings.


## -see-also




<a href="https://msdn.microsoft.com/79b57da4-0125-427b-aec7-7ca4c9bfb870">GLOBAL_MACHINE_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/0e89ae66-a889-4929-b028-125fcef5c89c">GLOBAL_USER_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/9a834fb6-35ae-4d36-885c-0d81cd39e9a6">GetCurrentPowerPolicies</a>



<a href="https://msdn.microsoft.com/65da3d9f-b688-4d41-9da0-05159297d169">ReadGlobalPwrPolicy</a>



<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a>



<a href="https://msdn.microsoft.com/293dc3a5-5e6b-4709-8439-67d2339740e7">WriteGlobalPwrPolicy</a>
 

 

