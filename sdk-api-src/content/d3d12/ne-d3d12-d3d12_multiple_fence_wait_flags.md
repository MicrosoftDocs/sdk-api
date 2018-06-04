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

# D3D12_MULTIPLE_FENCE_WAIT_FLAGS enumeration


## -description


Specifies multiple wait flags for multiple fences.


## -enum-fields




### -field D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE

Indicates that none of the fences need to be waited on.


### -field D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY

Indicates that any one of the fences need to be waited on.


### -field D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL

Indicates that all the fences need to be waited on.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/C187EEB7-DCD0-4535-AF0E-EF2C0E2DC83C">SetEventOnMultipleFenceCompletion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

