---
UID: NS:d3d12.D3D12_RESOURCE_ALIASING_BARRIER
title: D3D12_RESOURCE_ALIASING_BARRIER
author: windows-sdk-content
description: Describes the transition between usages of two different resources that have mappings into the same heap.
old-location: direct3d12\d3d12_resource_aliasing_barrier.htm
old-project: direct3d12
ms.assetid: 9855D609-E863-4334-B6BA-B6777FDAB82B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_RESOURCE_ALIASING_BARRIER, D3D12_RESOURCE_ALIASING_BARRIER structure, d3d12/D3D12_RESOURCE_ALIASING_BARRIER, direct3d12.d3d12_resource_aliasing_barrier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_RESOURCE_ALIASING_BARRIER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RESOURCE_ALIASING_BARRIER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_RESOURCE_ALIASING_BARRIER structure


## -description


Describes the transition between usages of two different resources that have mappings into the same heap.
        


## -struct-fields




### -field pResourceBefore

A pointer to the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> object that represents the before resource used in the transition.
          


### -field pResourceAfter

A pointer to the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> object that represents the after resource used in the transition.
          


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/49F02D65-767E-4BA4-A90D-68AA2D709E09">D3D12_RESOURCE_BARRIER</a> structure.
      

Both the before and the after resources can be specified or one or both resources can be <b>NULL</b>, which indicates that any placed or reserved resource could cause aliasing.
      

Refer to the usage models described in <a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

