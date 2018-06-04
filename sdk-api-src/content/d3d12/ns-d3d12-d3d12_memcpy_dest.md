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

# D3D12_MEMCPY_DEST structure


## -description



        Describes the destination of a memory copy operation.
      


## -struct-fields




### -field pData


            A pointer to a memory block that receives the copied data.
          


### -field RowPitch


            The row pitch, or width, or physical size, in bytes, of the subresource data.
          


### -field SlicePitch


            The slice pitch, or width, or physical size, in bytes, of the subresource data.
          


## -remarks



This structure is used by a number of helper methods, refer to <a href="https://msdn.microsoft.com/095958A9-345B-45AE-8363-B353534044B2">Helper Structures and Functions for D3D12</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

