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

# D3D12_RESOURCE_BARRIER_TYPE enumeration


## -description


Specifies a type of resource barrier (transition in resource use) description.


## -enum-fields




### -field D3D12_RESOURCE_BARRIER_TYPE_TRANSITION

A transition barrier that indicates a transition of a set of subresources between different usages. The caller must specify the before and after usages of the subresources. 


### -field D3D12_RESOURCE_BARRIER_TYPE_ALIASING

An aliasing barrier that indicates a transition between usages of 2 different resources that have mappings into the same tile pool. The caller can specify both the before and the after resource. Note that one or both resources can be <b>NULL</b>, which indicates that any tiled resource could cause aliasing.


### -field D3D12_RESOURCE_BARRIER_TYPE_UAV

An unordered access view (UAV) barrier that indicates all UAV accesses (reads or writes) to a particular resource must complete before any future UAV accesses (read or write) can begin. 


## -remarks



This enum is used in the <b>D3D12_RESOURCE_BARRIER_TYPE</b> structure. Use these values with the <a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ID3D12GraphicsCommandList::ResourceBarrier</a> method.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

