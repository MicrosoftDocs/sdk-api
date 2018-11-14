---
UID: NE:d3d11.D3D11_DSV_FLAG
title: D3D11_DSV_FLAG
author: windows-sdk-content
description: Depth-stencil view options.
old-location: direct3d11\d3d11_dsv_flag.htm
tech.root: direct3d11
ms.assetid: 8894ec55-9d56-4d41-a5d6-72ce064e3351
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_DSV_FLAG, D3D11_DSV_FLAG enumeration [Direct3D 11], D3D11_DSV_READ_ONLY_DEPTH, D3D11_DSV_READ_ONLY_STENCIL, d3d11/D3D11_DSV_FLAG, d3d11/D3D11_DSV_READ_ONLY_DEPTH, d3d11/D3D11_DSV_READ_ONLY_STENCIL, direct3d11.d3d11_dsv_flag, f62b0b22-d913-ed95-64ca-e81a26c5564b
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d11.h
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
 - D3D11.h
api_name:
 - D3D11_DSV_FLAG
product: Windows
targetos: Windows
req.typenames: D3D11_DSV_FLAG
req.redist: 
---

# D3D11_DSV_FLAG enumeration


## -description


Depth-stencil view options.


## -enum-fields




### -field D3D11_DSV_READ_ONLY_DEPTH

Indicates that depth values are read only.


### -field D3D11_DSV_READ_ONLY_STENCIL

Indicates that stencil values are read only.


## -remarks



This enumeration is used by <a href="https://msdn.microsoft.com/f073a798-edd5-4e6a-a8a7-1592721ce35d">D3D11_DEPTH_STENCIL_VIEW_DESC</a>.

Limiting a depth-stencil buffer to read-only access allows more than one depth-stencil view to be bound to the pipeline simultaneously, since it is not possible to have a read/write conflicts between separate views.




## -see-also




<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

