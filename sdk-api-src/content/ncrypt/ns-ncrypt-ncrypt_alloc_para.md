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

# NCRYPT_ALLOC_PARA structure


## -description


The <b>NCRYPT_ALLOC_PARA</b> structure enables you to specify custom functions that can be used to allocate and free data. This structure is used in the following functions:
<ul>
<li>
<a href="https://msdn.microsoft.com/EF4777D5-E218-4868-8D25-58E0EF8C9D30">NCryptGetProtectionDescriptorInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8726F92B-34D5-4696-8803-3D7F50F1006D">NCryptProtectSecret</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a>
</li>
</ul>

## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pfnAlloc

Address of a custom function that can allocate memory.


### -field pfnFree

Address of a function that can free memory allocated by the function specified by the <b>pfnAlloc</b> member.


## -see-also




<a href="https://msdn.microsoft.com/EF4777D5-E218-4868-8D25-58E0EF8C9D30">NCryptGetProtectionDescriptorInfo</a>



<a href="https://msdn.microsoft.com/8726F92B-34D5-4696-8803-3D7F50F1006D">NCryptProtectSecret</a>



<a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a>
 

 

