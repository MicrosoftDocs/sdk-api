---
UID: NS:d3d12.D3D12_RESOURCE_TRANSITION_BARRIER
title: D3D12_RESOURCE_TRANSITION_BARRIER
author: windows-driver-content
description: Describes the transition of subresources between different usages.
old-location: direct3d12\d3d12_resource_transition_barrier.htm
old-project: direct3d12
ms.assetid: 52C21198-827A-4E75-ADB8-DCA0204A4469
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: D3D12_RESOURCE_TRANSITION_BARRIER, D3D12_RESOURCE_TRANSITION_BARRIER structure, d3d12/D3D12_RESOURCE_TRANSITION_BARRIER, direct3d12.d3d12_resource_transition_barrier
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
req.typenames: D3D12_RESOURCE_TRANSITION_BARRIER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_RESOURCE_TRANSITION_BARRIER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_RESOURCE_TRANSITION_BARRIER structure


## -description



          Describes the transition of subresources between different usages.
        


## -struct-fields




### -field pResource


            A pointer to the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> object that represents the resource used in the transition.
          


### -field Subresource


            The index of the subresource for the transition.
            Use the <b>D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES</b> flag ( 0xffffffff ) to transition all subresources in a resource at the same time.
          


### -field StateBefore


            The "before" usages of the subresources, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
          


### -field StateAfter


            The "after" usages of the subresources, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
          


## -remarks




        This struct is used by the <b>Transition</b> member of the
        <a href="https://msdn.microsoft.com/49F02D65-767E-4BA4-A90D-68AA2D709E09">D3D12_RESOURCE_BARRIER</a> struct.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

