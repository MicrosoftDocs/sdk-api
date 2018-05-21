---
UID: NE:d3d12.D3D12_DESCRIPTOR_RANGE_TYPE
title: D3D12_DESCRIPTOR_RANGE_TYPE
author: windows-driver-content
description: Specifies a range so that, for example, if part of a descriptor table has 100 shader-resource views (SRVs) that range can be declared in one entry rather than 100.
old-location: direct3d12\d3d12_descriptor_range_type.htm
old-project: direct3d12
ms.assetid: A72AAEA7-D812-41D0-B9AD-8A219EC9A88A
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: D3D12_DESCRIPTOR_RANGE_TYPE, D3D12_DESCRIPTOR_RANGE_TYPE enumeration, D3D12_DESCRIPTOR_RANGE_TYPE_CBV, D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, D3D12_DESCRIPTOR_RANGE_TYPE_SRV, D3D12_DESCRIPTOR_RANGE_TYPE_UAV, d3d12/D3D12_DESCRIPTOR_RANGE_TYPE, d3d12/D3D12_DESCRIPTOR_RANGE_TYPE_CBV, d3d12/D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, d3d12/D3D12_DESCRIPTOR_RANGE_TYPE_SRV, d3d12/D3D12_DESCRIPTOR_RANGE_TYPE_UAV, direct3d12.d3d12_descriptor_range_type
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
req.typenames: D3D12_DESCRIPTOR_RANGE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_DESCRIPTOR_RANGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_DESCRIPTOR_RANGE_TYPE enumeration


## -description



          Specifies a range so that, for example, if part of a descriptor table has 100 shader-resource views (SRVs) that range can be declared in one entry rather than 100.
        


## -enum-fields




### -field D3D12_DESCRIPTOR_RANGE_TYPE_SRV


            Specifies a range of SRVs.
          


### -field D3D12_DESCRIPTOR_RANGE_TYPE_UAV


            Specifies a range of unordered-access views (UAVs).
          


### -field D3D12_DESCRIPTOR_RANGE_TYPE_CBV


            Specifies a range of constant-buffer views (CBVs).
          


### -field D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER


            Specifies a range of samplers.
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/6F1C4D05-3E08-4353-B5B9-4C4270FC1403">D3D12_DESCRIPTOR_RANGE</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

