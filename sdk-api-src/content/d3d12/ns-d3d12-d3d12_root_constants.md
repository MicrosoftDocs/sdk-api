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



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/F9A2640F-D1FA-481C-BDF1-B15372E3C512">Using constants directly in the root signature</a>
 

 

