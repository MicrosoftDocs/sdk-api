---
UID: NS:d3d12.D3D12_ROOT_DESCRIPTOR
title: D3D12_ROOT_DESCRIPTOR
author: windows-sdk-content
description: Describes descriptors inline in the root signature version 1.0 that appear in shaders.
old-location: direct3d12\d3d12_root_descriptor.htm
old-project: direct3d12
ms.assetid: F3ABC3B7-AD09-4CD6-9BE9-E30FAFD6E4F3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_ROOT_DESCRIPTOR, D3D12_ROOT_DESCRIPTOR structure, d3d12/D3D12_ROOT_DESCRIPTOR, direct3d12.d3d12_root_descriptor
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
req.typenames: D3D12_ROOT_DESCRIPTOR
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
req.lib: 
req.dll: 
req.irql: 
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



<b>D3D12_ROOT_DESCRIPTOR</b> is the data type of the <b>Descriptor</b> member of <a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a>.
        Use a <b>D3D12_ROOT_DESCRIPTOR</b> when you set <b>D3D12_ROOT_PARAMETER</b>'s <b>SlotType</b> field to the D3D12_ROOT_PARAMETER_TYPE_CBV, D3D12_ROOT_PARAMETER_TYPE_SRV, or D3D12_ROOT_PARAMETER_TYPE_UAV members of <a href="https://msdn.microsoft.com/1AC2D29E-3F94-4362-83B8-E9BE2175E42F">D3D12_ROOT_PARAMETER_TYPE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC">CD3DX12_ROOT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/55627E99-6EED-442F-93B8-D869F0B4EAF4">D3D12_ROOT_DESCRIPTOR1</a>



<a href="https://msdn.microsoft.com/033E3D8F-3003-42F7-BF77-68A7D62802E5">Using descriptors directly in the root signature</a>
 

 

