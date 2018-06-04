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

# D3D12_RESOLVE_MODE enumeration


## -description


Specifies a resolve operation.


## -enum-fields




### -field D3D12_RESOLVE_MODE_DECOMPRESS

Resolves compressed source samples to their uncompressed values. When using this operation, the source and destination resources must have the same sample count, unlike the min, max, and average operations that require the destination to have a sample count of 1.


### -field D3D12_RESOLVE_MODE_MIN

Resolves the source samples to their minimum value. It can be used with any render target or depth stencil format.


### -field D3D12_RESOLVE_MODE_MAX

Resolves the source samples to their maximum value. It can be used with any render target or depth stencil format.


### -field D3D12_RESOLVE_MODE_AVERAGE

Resolves the source samples to their average value. It can be used with any non-integer render target format, including the depth plane. It can't be used with integer render target formats, including the stencil plane.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/8CF3809C-0EC7-4FBB-AEEF-E74FCD9B836D">ID3D12GraphicsCommandList1::ResolveSubresourceRegion</a> function.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

