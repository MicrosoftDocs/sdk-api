---
UID: NS:d3d12.D3D12_RESOURCE_UAV_BARRIER
title: D3D12_RESOURCE_UAV_BARRIER
author: windows-driver-content
description: Represents a resource in which all UAV accesses must complete before any future UAV accesses can begin.
old-location: direct3d12\d3d12_resource_uav_barrier.htm
old-project: direct3d12
ms.assetid: 683F645F-9A90-4648-99EF-2F7444254B41
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_RESOURCE_UAV_BARRIER, D3D12_RESOURCE_UAV_BARRIER structure, d3d12/D3D12_RESOURCE_UAV_BARRIER, direct3d12.d3d12_resource_uav_barrier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3D12_RESOURCE_UAV_BARRIER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_RESOURCE_UAV_BARRIER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_RESOURCE_UAV_BARRIER structure


## -description



          Represents a resource in which all UAV accesses must complete before any future UAV accesses can begin.
        


## -struct-fields




### -field pResource


            The resource used in the transition, as a pointer to <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>.
          


## -remarks




        This struct represents a resource in which all unordered access view (UAV) accesses (reads or writes) must complete before any future UAV accesses (read or write) can begin.
      


        This structure is a member of the <a href="https://msdn.microsoft.com/49F02D65-767E-4BA4-A90D-68AA2D709E09">D3D12_RESOURCE_BARRIER</a> structure.
      


        You don't need to insert a UAV barrier between 2 draw or dispatch calls that only read a UAV.
        Additionally, you don't need to insert a UAV barrier between 2 draw or dispatch calls that write to the same UAV if you know that it's safe to execute the UAV accesses in any order.
        The resource can be <b>NULL</b>, which indicates that any UAV access could require the barrier.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

