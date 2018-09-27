---
UID: NE:d3d12.D3D12_TEXTURE_COPY_TYPE
title: D3D12_TEXTURE_COPY_TYPE
author: windows-sdk-content
description: Specifies what type of texture copy is to take place.
old-location: direct3d12\d3d12_texture_copy_type.htm
tech.root: direct3d12
ms.assetid: CF296200-55A7-46B2-BF2C-58806A6A3BBC
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D12_TEXTURE_COPY_TYPE, D3D12_TEXTURE_COPY_TYPE enumeration, D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT, D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX, d3d12/D3D12_TEXTURE_COPY_TYPE, d3d12/D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT, d3d12/D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX, direct3d12.d3d12_texture_copy_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - D3D12_TEXTURE_COPY_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_TEXTURE_COPY_TYPE
req.redist: 
---

# D3D12_TEXTURE_COPY_TYPE enumeration


## -description


Specifies what type of texture copy is to take place.


## -enum-fields




### -field D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX

Indicates a subresource, identified by an index, is to be copied.


### -field D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT

Indicates a place footprint, identified by a <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structure, is to be copied.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/D63EC731-EE75-44CD-9CCD-7FB4A761D1A3">D3D12_TEXTURE_COPY_LOCATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

