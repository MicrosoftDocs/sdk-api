---
UID: NE:d3d12.D3D12_CLEAR_FLAGS
title: D3D12_CLEAR_FLAGS
author: windows-sdk-content
description: Specifies what to clear from the depth stencil view.
old-location: direct3d12\d3d12_clear_flags.htm
tech.root: direct3d12
ms.assetid: F66672BC-1610-43F2-BF39-5F498183E3A5
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_CLEAR_FLAGS, D3D12_CLEAR_FLAGS enumeration, D3D12_CLEAR_FLAG_DEPTH, D3D12_CLEAR_FLAG_STENCIL, d3d12/D3D12_CLEAR_FLAGS, d3d12/D3D12_CLEAR_FLAG_DEPTH, d3d12/D3D12_CLEAR_FLAG_STENCIL, direct3d12.d3d12_clear_flags
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
 - d3d12.h
api_name:
 - D3D12_CLEAR_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_CLEAR_FLAGS
req.redist: 
---

# D3D12_CLEAR_FLAGS enumeration


## -description


Specifies what to clear from the depth stencil view.


## -enum-fields




### -field D3D12_CLEAR_FLAG_DEPTH

Indicates the depth buffer should be cleared.


### -field D3D12_CLEAR_FLAG_STENCIL

Indicates the stencil buffer should be cleared.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ID3D12GraphicsCommandList::ClearDepthStencilView</a>.
          The flags can be combined to clear all.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

