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

# D3D12_COMMAND_QUEUE_DESC structure


## -description


Describes a command queue.


## -struct-fields




### -field Type


            Specifies one member of <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE</a>.
          


### -field Priority


            The priority for the command queue, as a 
            <a href="https://msdn.microsoft.com/33C07FE4-D85F-4F94-BF0E-C9E0ED05765C">D3D12_COMMAND_QUEUE_PRIORITY</a>
            enumeration constant to select normal or high priority.
          


### -field Flags


            Specifies any flags from the <a href="https://msdn.microsoft.com/95040CB8-445B-4E10-8407-AA09637544FB">D3D12_COMMAND_QUEUE_FLAGS</a> enumeration.
          


### -field NodeMask


            For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter) to which the command queue applies.
            Each bit in the mask corresponds to a single node.
            Only 1 bit must be set.
          Refer to <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.


## -remarks




          This structure is passed into <a href="https://msdn.microsoft.com/556D068C-9939-4B42-AFC2-4EBB2D7B553B">CreateCommandQueue</a>.
        


          This structure is returned by <a href="https://msdn.microsoft.com/AEEE6B15-AEB0-47C5-A3F8-9957516BFBEE">ID3D12CommandQueue::GetDesc</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

