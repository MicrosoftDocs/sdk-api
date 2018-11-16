---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR
title: D3D12_ROOT_DESCRIPTOR
author: windows-sdk-content
description: Describes descriptors inline in the root signature version 1.0 that appear in shaders.
old-location: direct3d12\d3d12_root_descriptor.htm
tech.root: direct3d12
ms.assetid: F3ABC3B7-AD09-4CD6-9BE9-E30FAFD6E4F3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR, D3D12_ROOT_DESCRIPTOR structure, d3d12/D3D12_ROOT_DESCRIPTOR, direct3d12.d3d12_root_descriptor
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
 - D3D12.h
api_name:
 - D3D12_ROOT_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_DESCRIPTOR
req.redist: 
---

# D3D12_ROOT_DESCRIPTOR structure


## -description


Describes descriptors inline in the root signature version 1.0 that appear in shaders.
        


## -struct-fields




### -field ShaderRegister

The shader register.


### -field RegisterSpace

The register space.


## -remarks



<b>D3D12_ROOT_DESCRIPTOR</b> is the data type of the <b>Descriptor</b> member of <a href="https://msdn.microsoft.com/en-us/library/Dn879477(v=VS.85).aspx">D3D12_ROOT_PARAMETER</a>.
        Use a <b>D3D12_ROOT_DESCRIPTOR</b> when you set <b>D3D12_ROOT_PARAMETER</b>'s <b>SlotType</b> field to the D3D12_ROOT_PARAMETER_TYPE_CBV, D3D12_ROOT_PARAMETER_TYPE_SRV, or D3D12_ROOT_PARAMETER_TYPE_UAV members of <a href="https://msdn.microsoft.com/en-us/library/Dn879478(v=VS.85).aspx">D3D12_ROOT_PARAMETER_TYPE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt186579(v=VS.85).aspx">CD3DX12_ROOT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709120(v=VS.85).aspx">D3D12_ROOT_DESCRIPTOR1</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899223(v=VS.85).aspx">Using descriptors directly in the root signature</a>
 

 

