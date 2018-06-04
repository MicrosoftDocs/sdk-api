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

# D3D10_MAP_FLAG enumeration


## -description


Specifies how the CPU should respond when Map is called on a resource being used by the GPU.


## -enum-fields




### -field D3D10_MAP_FLAG_DO_NOT_WAIT

Specifies that Map should return <b>DXGI_ERROR_WAS_STILL_DRAWING</b> when the GPU blocks the CPU from accessing a resource.


## -remarks



This enumeration is used by <a href="https://msdn.microsoft.com/c863ef55-757d-4c0b-ba59-28d30499cf79">ID3D10Buffer::Map</a>, <a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">ID3D10Texture1D::Map</a>, <a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">ID3D10Texture2D::Map</a>, and <a href="https://msdn.microsoft.com/5cd7a5f0-4a74-4760-a709-d7941025699d">ID3D10Texture3D::Map</a>.

D3D10_MAP_FLAG_DO_NOT_WAIT cannot be used with <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP_WRITE_DISCARD</a> or <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP_WRITE_NOOVERWRITE</a>.

For more information about potential conflicts between the GPU and CPU during resource mapping, see <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">Copying and Accessing Resource Data (Direct3D 10)</a>.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

