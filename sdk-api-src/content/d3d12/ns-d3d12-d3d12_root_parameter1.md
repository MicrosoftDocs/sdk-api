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

# D3D12_ROOT_PARAMETER1 structure


## -description


Describes the slot of a root signature version 1.1.


## -struct-fields




### -field ParameterType


            A <a href="https://msdn.microsoft.com/1AC2D29E-3F94-4362-83B8-E9BE2175E42F">D3D12_ROOT_PARAMETER_TYPE</a>-typed value that  specifies the type of root signature slot. This member determines which type to use in the union below.
          


### -field DescriptorTable


              A <a href="https://msdn.microsoft.com/1D9D1846-2BE2-4B88-8D23-5A27173918DD">D3D12_ROOT_DESCRIPTOR_TABLE1</a> structure that describes the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.
            


### -field Constants


              A <a href="https://msdn.microsoft.com/B6630700-4F01-4D91-A8FF-3E9CB6505F51">D3D12_ROOT_CONSTANTS</a> structure that describes constants inline in the root signature that appear in shaders as one constant buffer.
            


### -field Descriptor


              A <a href="https://msdn.microsoft.com/55627E99-6EED-442F-93B8-D869F0B4EAF4">D3D12_ROOT_DESCRIPTOR1</a> structure that describes descriptors inline in the root signature that appear in shaders.
            


### -field ShaderVisibility


            A <a href="https://msdn.microsoft.com/1D66344A-110E-4190-BC00-9F88F1A3F8FB">D3D12_SHADER_VISIBILITY</a>-typed value that  specifies the shaders that can access the contents of the root signature slot.
          


## -remarks



Use this structure with the <a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a> structure.

Refer to the helper structure <a href="https://msdn.microsoft.com/CDE0C02E-0112-4FD9-A4A2-36E8C326715C">CD3DX12_ROOT_PARAMETER1</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

