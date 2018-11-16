---
UID: NE:d3d12.D3D12_DSV_FLAGS
title: D3D12_DSV_FLAGS
author: windows-sdk-content
description: Specifies depth-stencil view options.
old-location: direct3d12\d3d12_dsv_flags.htm
tech.root: direct3d12
ms.assetid: A968BFFF-8C26-4C8C-9AA4-7E9BB5B0DF1F
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_DSV_FLAGS, D3D12_DSV_FLAGS enumeration, D3D12_DSV_FLAG_NONE, D3D12_DSV_FLAG_READ_ONLY_DEPTH, D3D12_DSV_FLAG_READ_ONLY_STENCIL, d3d12/D3D12_DSV_FLAGS, d3d12/D3D12_DSV_FLAG_NONE, d3d12/D3D12_DSV_FLAG_READ_ONLY_DEPTH, d3d12/D3D12_DSV_FLAG_READ_ONLY_STENCIL, direct3d12.d3d12_dsv_flags
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D12.h
api_name:
 - D3D12_DSV_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_DSV_FLAGS
req.redist: 
---

# D3D12_DSV_FLAGS enumeration


## -description


Specifies depth-stencil view options.


## -enum-fields




### -field D3D12_DSV_FLAG_NONE

Indicates a default view.
          


### -field D3D12_DSV_FLAG_READ_ONLY_DEPTH

Indicates that depth values are read only.


### -field D3D12_DSV_FLAG_READ_ONLY_STENCIL

Indicates that stencil values are read only.


## -remarks



Specify a combination of the values in this enumeration in the <b>Flags</b> member of a <a href="https://msdn.microsoft.com/53161933-5B3B-4B38-AC70-46A4164AE072">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure.
          The values are combined by using a bitwise OR operation.
        

Limiting a depth-stencil buffer to read-only access allows more than one depth-stencil view to be bound to the pipeline simultaneously, since it is not possible to have read/write conflicts between separate views.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

