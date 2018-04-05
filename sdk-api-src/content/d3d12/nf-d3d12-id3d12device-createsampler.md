---
UID: NF:d3d12.ID3D12Device.CreateSampler
title: ID3D12Device::CreateSampler method
author: windows-driver-content
description: Create a sampler object that encapsulates sampling information for a texture.
old-location: direct3d12\id3d12device_createsampler.htm
old-project: direct3d12
ms.assetid: 453B2D3D-843E-4DB0-BC47-59BD9C78BFD6
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreateSampler method, CreateSampler method, ID3D12Device interface, CreateSampler,ID3D12Device.CreateSampler, ID3D12Device, ID3D12Device interface, CreateSampler method, ID3D12Device::CreateSampler, d3d12/ID3D12Device::CreateSampler, direct3d12.id3d12device_createsampler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D12.dll
api_name:
-	ID3D12Device.CreateSampler
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateSampler method


## -description


Create a sampler object that encapsulates sampling information for a texture.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/96261FE1-89D4-4135-B5C4-2D788DF4FA12">D3D12_SAMPLER_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/96261FE1-89D4-4135-B5C4-2D788DF4FA12">D3D12_SAMPLER_DESC</a> structure that describes the sampler. 


### -param DestDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the sampler.


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

