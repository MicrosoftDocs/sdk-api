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

# D3D12_SUBRESOURCE_FOOTPRINT structure


## -description



          Describes the format, width, height, depth, and row-pitch of the subresource into the parent resource.
        


## -struct-fields




### -field Format


            A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value that  specifies the viewing format.
          


### -field Width


            The width of the subresource.
          


### -field Height


            The height of the subresource.
          


### -field Depth


            The depth of the subresource.
          


### -field RowPitch


            The row pitch, or width, or physical size, in bytes, of the subresource data.
            This must be a multiple of D3D12_TEXTURE_DATA_PITCH_ALIGNMENT (256), and must be greater than or equal to the size of the data within a row.
          


## -remarks




        Use this structure in the <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structure.
      


        The helper structure is <a href="https://msdn.microsoft.com/17266FB0-41B5-4A70-A896-206B54F5E76F">CD3DX12_SUBRESOURCE_FOOTPRINT</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/17266FB0-41B5-4A70-A896-206B54F5E76F">CD3DX12_SUBRESOURCE_FOOTPRINT</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

