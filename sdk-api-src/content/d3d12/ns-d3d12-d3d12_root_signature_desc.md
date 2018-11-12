---
UID: NS:d3d12.D3D12_ROOT_SIGNATURE_DESC
title: D3D12_ROOT_SIGNATURE_DESC
author: windows-sdk-content
description: Describes the layout of a root signature version 1.0.
old-location: direct3d12\d3d12_root_signature_desc.htm
tech.root: direct3d12
ms.assetid: D74D9D3B-96AB-489A-A91C-4F68AC3D05EE
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_ROOT_SIGNATURE_DESC, D3D12_ROOT_SIGNATURE_DESC structure, d3d12/D3D12_ROOT_SIGNATURE_DESC, direct3d12.d3d12_root_signature_desc
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

An array of <a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a> structures for the slots in the root signature.
          


### -field NumStaticSamplers

Specifies the number of static samplers.


### -field pStaticSamplers

Pointer to one or more <a href="https://msdn.microsoft.com/35553C1C-3661-4778-8BC5-F2E6775DF96D">D3D12_STATIC_SAMPLER_DESC</a> structures.
          


### -field Flags

A combination of <a href="https://msdn.microsoft.com/C3118E58-2006-459F-B2D6-4EC84F2BC058">D3D12_ROOT_SIGNATURE_FLAGS</a>-typed values that are combined by using a bitwise OR operation.
            The resulting value specifies options for the root signature layout.
          


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/ACC46F5E-1074-41B3-8D13-9FD4352DBF66">D3D12SerializeRootSignature</a> function
        and is returned by the <a href="https://msdn.microsoft.com/A13FB848-A5C1-4B9B-9009-B0166A3A1C8D">ID3D12RootSignatureDeserializer::GetRootSignatureDesc</a> method.
      

There is one graphics root signature, and one compute root signature.
      




## -see-also




<a href="https://msdn.microsoft.com/A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F">CD3DX12_ROOT_SIGNATURE_DESC</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/1AC2D29E-3F94-4362-83B8-E9BE2175E42F">D3D12_ROOT_PARAMETER_TYPE</a>



<a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a>



<a href="https://msdn.microsoft.com/F9A2640F-D1FA-481C-BDF1-B15372E3C512">Using constants directly in the root signature</a>



<a href="https://msdn.microsoft.com/033E3D8F-3003-42F7-BF77-68A7D62802E5">Using descriptors directly in the root signature</a>
 

 

