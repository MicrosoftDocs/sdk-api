---
UID: NS:d3d12.D3D12_COMMAND_QUEUE_DESC
title: D3D12_COMMAND_QUEUE_DESC (d3d12.h)
author: windows-sdk-content
description: Describes a command queue.
old-location: direct3d12\d3d12_command_queue_desc.htm
tech.root: direct3d12
ms.assetid: 8C43C45B-0A7B-4336-B546-1E6F13D153F3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_COMMAND_QUEUE_DESC, D3D12_COMMAND_QUEUE_DESC structure, d3d12/D3D12_COMMAND_QUEUE_DESC, direct3d12.d3d12_command_queue_desc
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
 - d3d12.h
api_name:
 - D3D12_COMMAND_QUEUE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_COMMAND_QUEUE_DESC
req.redist: 
---

# D3D12_COMMAND_QUEUE_DESC structure


## -description


Describes a command queue.


## -struct-fields




### -field Type

Specifies one member of <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE</a>.
          


### -field Priority

The priority for the command queue, as a 
            <a href="https://msdn.microsoft.com/33C07FE4-D85F-4F94-BF0E-C9E0ED05765C">D3D12_COMMAND_QUEUE_PRIORITY</a>enumeration constant to select normal or high priority.
          


### -field Flags

Specifies any flags from the <a href="https://msdn.microsoft.com/95040CB8-445B-4E10-8407-AA09637544FB">D3D12_COMMAND_QUEUE_FLAGS</a> enumeration.
          


### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter) to which the command queue applies.
            Each bit in the mask corresponds to a single node.
            Only 1 bit must be set.
          Refer to <a href="https://msdn.microsoft.com/en-us/library/Dn933253(v=VS.85).aspx">Multi-Adapter</a>.


## -remarks



This structure is passed into <a href="https://msdn.microsoft.com/556D068C-9939-4B42-AFC2-4EBB2D7B553B">CreateCommandQueue</a>.
        

This structure is returned by <a href="https://msdn.microsoft.com/AEEE6B15-AEB0-47C5-A3F8-9957516BFBEE">ID3D12CommandQueue::GetDesc</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

