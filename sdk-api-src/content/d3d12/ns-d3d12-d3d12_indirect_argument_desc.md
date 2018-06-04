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

# D3D12_INDIRECT_ARGUMENT_DESC structure


## -description



          Describes an indirect argument (an indirect parameter), for use with a command signature.
        


## -struct-fields




### -field Type


            A single <a href="https://msdn.microsoft.com/03324A50-BE16-4FC0-BFE7-9EE97C738165">D3D12_INDIRECT_ARGUMENT_TYPE</a> enumeration constant.
          


### -field VertexBuffer


### -field VertexBuffer.Slot


                Specifies the slot containing the vertex buffer address.
              


### -field Constant


### -field Constant.RootParameterIndex


                Specifies the root index of the constant.
              


### -field Constant.DestOffsetIn32BitValues


                The offset, in 32-bit values, to set the first constant of the group.
                Supports multi-value constants at a given root index.
                Root constant entries must be sorted from smallest to largest DestOffsetIn32BitValues.
              


### -field Constant.Num32BitValuesToSet


                The number of 32-bit constants that are set at the given root index.
                Supports multi-value constants at a given root index.
              


### -field ConstantBufferView


### -field ConstantBufferView.RootParameterIndex


                Specifies the root index of the CBV.
              


### -field ShaderResourceView


### -field ShaderResourceView.RootParameterIndex


                Specifies the root index of the SRV.
              


### -field UnorderedAccessView


### -field UnorderedAccessView.RootParameterIndex


                Specifies the root index of the UAV.
              


## -remarks




          Use this structure with the <a href="https://msdn.microsoft.com/3ACB1582-7A93-4D8D-A463-A828EF0C7F92">D3D12_COMMAND_SIGNATURE_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/493D35C9-2A90-4688-BD7E-74B9EB2B4E72">Example Root Signatures</a>
 

 

