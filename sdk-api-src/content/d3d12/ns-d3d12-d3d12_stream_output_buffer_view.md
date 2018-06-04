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

# D3D12_STREAM_OUTPUT_BUFFER_VIEW structure


## -description



          Describes a stream output buffer.
        


## -struct-fields




### -field BufferLocation


            A D3D12_GPU_VIRTUAL_ADDRESS (a UINT64) that points to the stream output buffer.
            If <b>SizeInBytes</b> is 0, this member isn't used and can be any value.
          


### -field SizeInBytes


            The size of the stream output buffer in bytes.
          


### -field BufferFilledSizeLocation


            The location of the value of how much data has been filled into the buffer, as a D3D12_GPU_VIRTUAL_ADDRESS (a UINT64).
            This member can't be NULL; a filled size location must be supplied (which the hardware will increment as data is output).
            If <b>SizeInBytes</b> is 0, this member isn't used and can be any value.
          


## -remarks




          Use this structure with <a href="https://msdn.microsoft.com/40683FD6-5B9F-411C-AC0A-6641E0A3D688">SOSetTargets</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

