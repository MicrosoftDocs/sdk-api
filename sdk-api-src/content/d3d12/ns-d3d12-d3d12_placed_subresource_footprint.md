---
UID: NS:d3d12.D3D12_PLACED_SUBRESOURCE_FOOTPRINT
title: D3D12_PLACED_SUBRESOURCE_FOOTPRINT (d3d12.h)
author: windows-sdk-content
description: Describes the footprint of a placed subresource, including the offset and the D3D12_SUBRESOURCE_FOOTPRINT.
old-location: direct3d12\d3d12_placed_subresource_footprint.htm
tech.root: direct3d12
ms.assetid: 74740A52-C2A5-4AF6-92CC-85B5C214423F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_PLACED_SUBRESOURCE_FOOTPRINT, D3D12_PLACED_SUBRESOURCE_FOOTPRINT structure, d3d12/D3D12_PLACED_SUBRESOURCE_FOOTPRINT, direct3d12.d3d12_placed_subresource_footprint
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
 - D3D12_PLACED_SUBRESOURCE_FOOTPRINT
product: Windows
targetos: Windows
req.typenames: D3D12_PLACED_SUBRESOURCE_FOOTPRINT
req.redist: 
---

# D3D12_PLACED_SUBRESOURCE_FOOTPRINT structure


## -description


Describes the footprint of a placed subresource, including the offset and the D3D12_SUBRESOURCE_FOOTPRINT.
        


## -struct-fields




### -field Offset

The offset of the subresource within the parent resource, in bytes.
            The offset between the start of the parent resource and this subresource.
          


### -field Footprint

The format, width, height, depth, and row-pitch of the subresource,
            as a <a href="https://msdn.microsoft.com/C73B6AB0-F9C5-432E-BA26-3B7772411C95">D3D12_SUBRESOURCE_FOOTPRINT</a> structure.
          


## -remarks



This structure is used in the <a href="https://msdn.microsoft.com/D63EC731-EE75-44CD-9CCD-7FB4A761D1A3">D3D12_TEXTURE_COPY_LOCATION</a> structure,
          and by <a href="https://msdn.microsoft.com/EB3715A9-5A73-45DA-A46F-7889188409A3">ID3D12Device::GetCopyableFootprints</a>.
        

All the data referenced by the footprint structure must fit within the bounds of the parent resource. If you use <a href="https://msdn.microsoft.com/EB3715A9-5A73-45DA-A46F-7889188409A3">GetCopyableFootprints</a> to fill out the structure, the <i>pTotalBytes</i> output field indicates the required size of the resource.

This structure is also used a number of helper functions (refer to <a href="https://msdn.microsoft.com/095958A9-345B-45AE-8363-B353534044B2">Helper Structures and Functions for D3D12</a>).

When copying textures, use this structure along with <a href="https://msdn.microsoft.com/D63EC731-EE75-44CD-9CCD-7FB4A761D1A3">D3D12_TEXTURE_COPY_LOCATION</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

