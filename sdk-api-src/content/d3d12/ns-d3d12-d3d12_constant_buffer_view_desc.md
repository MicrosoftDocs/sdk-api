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

# D3D12_CONSTANT_BUFFER_VIEW_DESC structure


## -description


Describes a constant buffer to view.


## -struct-fields




### -field BufferLocation


            The D3D12_GPU_VIRTUAL_ADDRESS of the constant buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.
          


### -field SizeInBytes

The size in bytes of the constant buffer.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/13251F82-4AE9-4234-A0C8-0E666F8A1856">CreateConstantBufferView</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

