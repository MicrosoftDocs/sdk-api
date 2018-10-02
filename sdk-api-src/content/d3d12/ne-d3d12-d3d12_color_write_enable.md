---
UID: NE:d3d12.D3D12_COLOR_WRITE_ENABLE
title: D3D12_COLOR_WRITE_ENABLE
author: windows-sdk-content
description: Identifies which components of each pixel of a render target are writable during blending.
old-location: direct3d12\d3d12_color_write_enable.htm
tech.root: direct3d12
ms.assetid: BC07C5E7-CFEC-4902-9FB1-74A4396190BC
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_COLOR_WRITE_ENABLE, D3D12_COLOR_WRITE_ENABLE enumeration, D3D12_COLOR_WRITE_ENABLE_ALL, D3D12_COLOR_WRITE_ENABLE_ALPHA, D3D12_COLOR_WRITE_ENABLE_BLUE, D3D12_COLOR_WRITE_ENABLE_GREEN, D3D12_COLOR_WRITE_ENABLE_RED, d3d12/D3D12_COLOR_WRITE_ENABLE, d3d12/D3D12_COLOR_WRITE_ENABLE_ALL, d3d12/D3D12_COLOR_WRITE_ENABLE_ALPHA, d3d12/D3D12_COLOR_WRITE_ENABLE_BLUE, d3d12/D3D12_COLOR_WRITE_ENABLE_GREEN, d3d12/D3D12_COLOR_WRITE_ENABLE_RED, direct3d12.d3d12_color_write_enable
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
 - D3D12.h
api_name:
 - D3D12_COLOR_WRITE_ENABLE
product: Windows
targetos: Windows
req.typenames: D3D12_COLOR_WRITE_ENABLE
req.redist: 
---

# D3D12_COLOR_WRITE_ENABLE enumeration


## -description


Identifies which components of each pixel of a render target are writable during blending.


## -enum-fields




### -field D3D12_COLOR_WRITE_ENABLE_RED

Allow data to be stored in the red component.


### -field D3D12_COLOR_WRITE_ENABLE_GREEN

Allow data to be stored in the green component.


### -field D3D12_COLOR_WRITE_ENABLE_BLUE

Allow data to be stored in the blue component.


### -field D3D12_COLOR_WRITE_ENABLE_ALPHA

Allow data to be stored in the alpha component.


### -field D3D12_COLOR_WRITE_ENABLE_ALL

Allow data to be stored in all components.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/911158CF-5F4F-4211-8CC6-F73BDB697BC5">D3D12_RENDER_TARGET_BLEND_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/D37BB62E-904B-4953-9119-21F3B37570C0">CD3DX12_BLEND_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

