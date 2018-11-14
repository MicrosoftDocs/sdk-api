---
UID: NS:d3d12.D3D12_ROOT_SIGNATURE_DESC
title: D3D12_ROOT_SIGNATURE_DESC
author: windows-sdk-content
description: Describes the layout of a root signature version 1.0.
old-location: direct3d12\d3d12_root_signature_desc.htm
tech.root: direct3d12
ms.assetid: D74D9D3B-96AB-489A-A91C-4F68AC3D05EE
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_ROOT_SIGNATURE_DESC, D3D12_ROOT_SIGNATURE_DESC structure, d3d12/D3D12_ROOT_SIGNATURE_DESC, direct3d12.d3d12_root_signature_desc
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
 - D3D12_ROOT_SIGNATURE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_ROOT_SIGNATURE_DESC
req.redist: 
---

# D3D12_ROOT_SIGNATURE_DESC structure


## -description


Describes the layout of a root signature version 1.0.
        


## -struct-fields




### -field NumParameters

The number of slots in the root signature. This number is also the number of elements in the <i>pParameters</i> array.
          


### -field pParameters

An array of <a href="https://msdn.microsoft.com/en-us/library/Dn879477(v=VS.85).aspx">D3D12_ROOT_PARAMETER</a> structures for the slots in the root signature.
          


### -field NumStaticSamplers

Specifies the number of static samplers.


### -field pStaticSamplers

Pointer to one or more <a href="https://msdn.microsoft.com/en-us/library/Dn986748(v=VS.85).aspx">D3D12_STATIC_SAMPLER_DESC</a> structures.
          


### -field Flags

A combination of <a href="https://msdn.microsoft.com/en-us/library/Dn879480(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_FLAGS</a>-typed values that are combined by using a bitwise OR operation.
            The resulting value specifies options for the root signature layout.
          


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/en-us/library/Dn859363(v=VS.85).aspx">D3D12SerializeRootSignature</a> function
        and is returned by the <a href="https://msdn.microsoft.com/en-us/library/Dn986887(v=VS.85).aspx">ID3D12RootSignatureDeserializer::GetRootSignatureDesc</a> method.
      

There is one graphics root signature, and one compute root signature.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt186582(v=VS.85).aspx">CD3DX12_ROOT_SIGNATURE_DESC</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859357(v=VS.85).aspx">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn879478(v=VS.85).aspx">D3D12_ROOT_PARAMETER_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709124(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC1</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899219(v=VS.85).aspx">Using constants directly in the root signature</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899223(v=VS.85).aspx">Using descriptors directly in the root signature</a>
 

 

