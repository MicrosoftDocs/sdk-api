---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_DESCRIPTOR_RANGE1 structure


## -description


Describes a descriptor range, with flags to determine their volatility.


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
          


### -field Flags

Specifies the <a href="https://msdn.microsoft.com/B22DBE80-A0BE-40F9-ADC2-5AFB35DDDDE8">D3D12_DESCRIPTOR_RANGE_FLAGS</a> that determine descriptor and data volatility.


### -field OffsetInDescriptorsFromTableStart


            The offset in descriptors from the start of the root signature. This value can be <b>D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND</b>, which indicates this range should immediately follow the preceding range.


## -remarks




        This structure is a member of the <a href="https://msdn.microsoft.com/1D9D1846-2BE2-4B88-8D23-5A27173918DD">D3D12_ROOT_DESCRIPTOR_TABLE1</a> structure.
      

Refer to the helper structure <a href="https://msdn.microsoft.com/9D073158-5907-4D1C-8D75-72B304277DAD">CD3DX12_DESCRIPTOR_RANGE1</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

