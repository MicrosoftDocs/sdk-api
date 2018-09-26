---
UID: NS:d3d12.D3D12_BOX
title: D3D12_BOX
author: windows-sdk-content
description: Describes a 3D box.
old-location: direct3d12\d3d12_box.htm
tech.root: direct3d12
ms.assetid: DD3973CC-043E-486E-9403-B46D8B7DE644
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_BOX, D3D12_BOX structure, d3d12/D3D12_BOX, direct3d12.d3d12_box
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
 - D3D12_BOX
product: Windows
targetos: Windows
req.typenames: D3D12_BOX
req.redist: 
---

# D3D12_BOX structure


## -description


Describes a 3D box.


## -struct-fields




### -field left

The x position of the left hand side of the box.


### -field top

The y position of the top of the box.


### -field front

The z position of the front of the box.


### -field right

The x position of the right hand side of the box, plus 1. This means that <code>right - left</code> equals the width of the box.


### -field bottom

The y position of the bottom of the box, plus 1. This means that <code>top - bottom</code> equals the height of the box.


### -field back

The z position of the back of the box, plus 1. This means that <code>front - back</code> equals the depth of the box.


## -remarks



This structure is used by the methods <a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a>, <a href="https://msdn.microsoft.com/A1F61217-A383-49BF-B675-FBC7F6D015DB">ReadFromSubresource</a> and <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7E1A352C-D664-4538-BA78-91493980559D">CD3DX12_BOX</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

