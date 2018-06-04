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
 

 

