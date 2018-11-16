---
UID: NS:d3d10.D3D10_BUFFER_SRV
title: D3D10_BUFFER_SRV
author: windows-sdk-content
description: Specifies the elements in a buffer resource to use in a shader-resource view.
old-location: direct3d10\d3d10_buffer_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_buffer_srv.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 2f5305b7-1dcd-3d82-23b3-875654ce7066, D3D10_BUFFER_SRV, D3D10_BUFFER_SRV structure [Direct3D 10], d3d10/D3D10_BUFFER_SRV, direct3d10.d3d10_buffer_srv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10.h
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
 - D3D10.h
api_name:
 - D3D10_BUFFER_SRV
product: Windows
targetos: Windows
req.typenames: D3D10_BUFFER_SRV
req.redist: 
---

# D3D10_BUFFER_SRV structure


## -description


Specifies the elements in a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffer</a> resource to use in a shader-resource view.


## -struct-fields




### -field FirstElement

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of bytes between the beginning of the buffer and the first element to access.


### -field ElementOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset of the first element in the view to access, relative to element 0.


### -field NumElements

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The total number of elements in the view.


### -field ElementWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width of each element (in bytes). This can be determined from the format stored in the shader-resource-view description.


## -remarks



The <b>D3D10_BUFFER_SRV</b> structure is a member of the  <a href="https://msdn.microsoft.com/en-us/library/Bb172437(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC</a> structure, which represents a shader-resource view description. You can create a shader-resource view by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb173558(v=VS.85).aspx">ID3D10Device::CreateShaderResourceView</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

