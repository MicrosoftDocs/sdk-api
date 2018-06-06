---
UID: NS:d3d12.D3D12_SUBRESOURCE_FOOTPRINT
title: D3D12_SUBRESOURCE_FOOTPRINT
author: windows-sdk-content
description: Describes the format, width, height, depth, and row-pitch of the subresource into the parent resource.
old-location: direct3d12\d3d12_subresource_footprint.htm
old-project: direct3d12
ms.assetid: C73B6AB0-F9C5-432E-BA26-3B7772411C95
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_SUBRESOURCE_FOOTPRINT, D3D12_SUBRESOURCE_FOOTPRINT structure, d3d12/D3D12_SUBRESOURCE_FOOTPRINT, direct3d12.d3d12_subresource_footprint
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
tech.root: 
req.typenames: D3D12_SUBRESOURCE_FOOTPRINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SUBRESOURCE_FOOTPRINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

