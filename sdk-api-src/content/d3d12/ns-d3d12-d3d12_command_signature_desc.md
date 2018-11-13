---
UID: NS:d3d12.D3D12_COMMAND_SIGNATURE_DESC
title: D3D12_COMMAND_SIGNATURE_DESC
author: windows-sdk-content
description: Describes the arguments (parameters) of a command signature.
old-location: direct3d12\d3d12_command_signature_desc.htm
tech.root: direct3d12
ms.assetid: 3ACB1582-7A93-4D8D-A463-A828EF0C7F92
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_COMMAND_SIGNATURE_DESC, D3D12_COMMAND_SIGNATURE_DESC structure, d3d12/D3D12_COMMAND_SIGNATURE_DESC, direct3d12.d3d12_command_signature_desc
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
 - D3D12_COMMAND_SIGNATURE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_COMMAND_SIGNATURE_DESC
req.redist: 
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
 

 

