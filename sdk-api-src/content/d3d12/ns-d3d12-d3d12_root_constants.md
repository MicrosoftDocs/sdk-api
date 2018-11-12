---
UID: NS:d3d12.D3D12_ROOT_CONSTANTS
title: D3D12_ROOT_CONSTANTS
author: windows-sdk-content
description: Describes constants inline in the root signature that appear in shaders as one constant buffer.
old-location: direct3d12\d3d12_root_constants.htm
tech.root: direct3d12
ms.assetid: B6630700-4F01-4D91-A8FF-3E9CB6505F51
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_ROOT_CONSTANTS, D3D12_ROOT_CONSTANTS structure, d3d12/D3D12_ROOT_CONSTANTS, direct3d12.d3d12_root_constants
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D12_ROOT_CONSTANTS
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_CONSTANTS
req.redist: 
---

# D3D12_ROOT_CONSTANTS structure


## -description


Describes constants inline in the root signature that appear in shaders as one constant buffer.
        


## -struct-fields




### -field ShaderRegister

The shader register.
          


### -field RegisterSpace

The register space.
          


### -field Num32BitValues

The number of constants that occupy a single shader slot (these constants appear like a single constant buffer). 
            All constants occupy a single root signature bind slot.
          


## -remarks



Refer to <a href="https://msdn.microsoft.com/3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9">Resource Binding in HLSL</a> for more information on shader registers and spaces. 

<b>D3D12_ROOT_CONSTANTS</b> is the data type of the <b>Constants</b> member of <a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a>. 
        Use a <b>D3D12_ROOT_CONSTANTS</b> when you set <b>D3D12_ROOT_PARAMETER</b>'s <b>SlotType</b> field to the D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS member of <a href="https://msdn.microsoft.com/1AC2D29E-3F94-4362-83B8-E9BE2175E42F">D3D12_ROOT_PARAMETER_TYPE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/2F517DCE-BC0C-4678-9C25-D826036F99A8">CD3DX12_ROOT_CONSTANTS</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859357(v=VS.85).aspx">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899219(v=VS.85).aspx">Using constants directly in the root signature</a>
 

 

