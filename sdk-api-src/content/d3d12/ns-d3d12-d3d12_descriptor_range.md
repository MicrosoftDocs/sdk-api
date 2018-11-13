---
UID: NS:d3d12.D3D12_DESCRIPTOR_RANGE
title: D3D12_DESCRIPTOR_RANGE
author: windows-sdk-content
description: Describes a descriptor range.
old-location: direct3d12\d3d12_descriptor_range.htm
tech.root: direct3d12
ms.assetid: 6F1C4D05-3E08-4353-B5B9-4C4270FC1403
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_DESCRIPTOR_RANGE, D3D12_DESCRIPTOR_RANGE structure, d3d12/D3D12_DESCRIPTOR_RANGE, direct3d12.d3d12_descriptor_range
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
 - D3D12_DESCRIPTOR_RANGE
product: Windows
targetos: Windows
req.typenames: D3D12_DESCRIPTOR_RANGE
req.redist: 
---

# D3D12_DESCRIPTOR_RANGE structure


## -description


Describes a descriptor range.


## -struct-fields




### -field RangeType

A <a href="https://msdn.microsoft.com/A72AAEA7-D812-41D0-B9AD-8A219EC9A88A">D3D12_DESCRIPTOR_RANGE_TYPE</a>-typed value that specifies the type of descriptor range.
          


### -field NumDescriptors

The number of descriptors in the range. Use -1 or UINT_MAX to specify unbounded size. Only the last entry in a table can have unbounded size.
          


### -field BaseShaderRegister

The base shader register in the range. For example, for shader-resource views (SRVs), 3 maps to ": register(t3);" in HLSL.
          


### -field RegisterSpace

The register space. Can typically be 0, but allows multiple descriptor  arrays of unknown size to not appear to overlap.
            For example, for SRVs, by extending the example in the <b>BaseShaderRegister</b> member description, 5 maps to ": register(t3,space5);" in HLSL.
          


### -field OffsetInDescriptorsFromTableStart

The offset in descriptors from the start of the root signature. This value can be <b>D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND</b>, which indicates this range should immediately follow the preceding range.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/5A0A04AB-2053-40E0-9CD5-E344BFE9001E">D3D12_ROOT_DESCRIPTOR_TABLE</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/F066ECA5-5E52-4483-B773-B43C5F12809B">CD3DX12_DESCRIPTOR_RANGE</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

