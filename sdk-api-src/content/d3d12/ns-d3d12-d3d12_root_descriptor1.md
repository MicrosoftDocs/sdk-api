---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR1
title: D3D12_ROOT_DESCRIPTOR1
author: windows-sdk-content
description: Describes descriptors inline in the root signature version 1.1 that appear in shaders.
old-location: direct3d12\d3d12_root_descriptor1.htm
tech.root: direct3d12
ms.assetid: 55627E99-6EED-442F-93B8-D869F0B4EAF4
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR1, D3D12_ROOT_DESCRIPTOR1 structure, d3d12/D3D12_ROOT_DESCRIPTOR1, direct3d12.d3d12_root_descriptor1
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_ROOT_DESCRIPTOR1
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_DESCRIPTOR1
req.redist: 
---

# D3D12_ROOT_DESCRIPTOR1 structure


## -description


Describes descriptors inline in the root signature version 1.1 that appear in shaders.
        


## -struct-fields




### -field ShaderRegister

The shader register.


### -field RegisterSpace

The register space.


### -field Flags

Specifies the <a href="https://msdn.microsoft.com/1BF4D1FA-C938-4704-8D82-CFCA6FE954CB">D3D12_ROOT_DESCRIPTOR_FLAGS</a> that determine the volatility of descriptors and the data they reference.


## -remarks



<b>D3D12_ROOT_DESCRIPTOR1</b> is the data type of the <b>Descriptor</b> member of <a href="https://msdn.microsoft.com/615B8ABF-FD80-4254-976B-9E587CE9F12E">D3D12_ROOT_PARAMETER1</a>.
        Use a <b>D3D12_ROOT_DESCRIPTOR1</b> when you set <b>D3D12_ROOT_PARAMETER1</b>'s <b>SlotType</b> field to the D3D12_ROOT_PARAMETER_TYPE_CBV, D3D12_ROOT_PARAMETER_TYPE_SRV, or D3D12_ROOT_PARAMETER_TYPE_UAV members of <a href="https://msdn.microsoft.com/1AC2D29E-3F94-4362-83B8-E9BE2175E42F">D3D12_ROOT_PARAMETER_TYPE</a>.
      

Refer to the helper structure <a href="https://msdn.microsoft.com/664822BF-5C27-4541-953F-219894547A6C">CD3DX12_ROOT_DESCRIPTOR1</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/F3ABC3B7-AD09-4CD6-9BE9-E30FAFD6E4F3">D3D12_ROOT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

