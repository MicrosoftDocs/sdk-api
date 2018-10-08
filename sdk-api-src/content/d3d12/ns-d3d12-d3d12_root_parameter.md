---
UID: NS:d3d12.D3D12_ROOT_PARAMETER
title: D3D12_ROOT_PARAMETER
author: windows-sdk-content
description: Describes the slot of a root signature version 1.0.
old-location: direct3d12\d3d12_root_parameter.htm
tech.root: direct3d12
ms.assetid: CC1DFE85-7F83-4551-86C6-1AFDF746FC92
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D12_ROOT_PARAMETER, D3D12_ROOT_PARAMETER structure, d3d12/D3D12_ROOT_PARAMETER, direct3d12.d3d12_root_parameter
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
 - D3D12_ROOT_PARAMETER
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_PARAMETER
req.redist: 
---

# D3D12_ROOT_PARAMETER structure


## -description


Describes the slot of a root signature version 1.0.


## -struct-fields




### -field ParameterType

A <a href="https://msdn.microsoft.com/en-us/library/Dn879478(v=VS.85).aspx">D3D12_ROOT_PARAMETER_TYPE</a>-typed value that  specifies the type of root signature slot. This member determines which type to use in the union below.
          


### -field DescriptorTable

A <a href="https://msdn.microsoft.com/en-us/library/Dn859382(v=VS.85).aspx">D3D12_ROOT_DESCRIPTOR_TABLE</a> structure that describes the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
            


### -field Constants

A <a href="https://msdn.microsoft.com/en-us/library/Dn879475(v=VS.85).aspx">D3D12_ROOT_CONSTANTS</a> structure that describes constants inline in the root signature that appear in shaders as one constant buffer.
            


### -field Descriptor

A <a href="https://msdn.microsoft.com/en-us/library/Dn879476(v=VS.85).aspx">D3D12_ROOT_DESCRIPTOR</a> structure that describes descriptors inline in the root signature that appear in shaders.
            


### -field ShaderVisibility

A <a href="https://msdn.microsoft.com/en-us/library/Dn879482(v=VS.85).aspx">D3D12_SHADER_VISIBILITY</a>-typed value that  specifies the shaders that can access the contents of the root signature slot.
          


## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/Dn986747(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC</a> can contain descriptor tables and inline constants. More capable hardware could support inline descriptors in the root signature as well. The number of bind slots in the root signature are most efficient if kept below a certain size, and can have an upper bound as well.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt186581(v=VS.85).aspx">CD3DX12_ROOT_PARAMETER</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859357(v=VS.85).aspx">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709123(v=VS.85).aspx">D3D12_ROOT_PARAMETER1</a>
 

 

