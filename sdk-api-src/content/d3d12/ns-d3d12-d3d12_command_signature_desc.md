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

# D3D12_COMMAND_SIGNATURE_DESC structure


## -description



          Describes the arguments (parameters) of a command signature.
        


## -struct-fields




### -field ByteStride


            Specifies the size of each argument of a command signature, in bytes.
          


### -field NumArgumentDescs


            Specifies the number of arguments in the command signature.
          


### -field pArgumentDescs


            An array of <a href="https://msdn.microsoft.com/2B51E4B1-F48A-4937-A92D-6AE9449018B4">D3D12_INDIRECT_ARGUMENT_DESC</a> structures,
            containing details of the arguments, including whether the argument is a vertex buffer, constant, constant buffer view, shader resource view, or unordered access view.
          


### -field NodeMask


            For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) for which the command signature is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.


## -remarks




          Use this structure by <a href="https://msdn.microsoft.com/5A44F907-C6E0-4548-A227-84F0CF2EE837">CreateCommandSignature</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

