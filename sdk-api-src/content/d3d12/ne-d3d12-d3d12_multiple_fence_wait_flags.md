---
UID: NE:d3d12.D3D12_MULTIPLE_FENCE_WAIT_FLAGS
title: D3D12_MULTIPLE_FENCE_WAIT_FLAGS
author: windows-driver-content
description: Specifies multiple wait flags for multiple fences.
old-location: direct3d12\d3d12_multiple_fence_wait_flags.htm
old-project: direct3d12
ms.assetid: A5C52F58-C082-41C2-99E4-800DFBA250D2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_MULTIPLE_FENCE_WAIT_FLAGS, D3D12_MULTIPLE_FENCE_WAIT_FLAGS enumeration, D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL, D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY, D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAGS, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_ALL, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_ANY, d3d12/D3D12_MULTIPLE_FENCE_WAIT_FLAG_NONE, direct3d12.d3d12_multiple_fence_wait_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D12_MULTIPLE_FENCE_WAIT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_MULTIPLE_FENCE_WAIT_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

