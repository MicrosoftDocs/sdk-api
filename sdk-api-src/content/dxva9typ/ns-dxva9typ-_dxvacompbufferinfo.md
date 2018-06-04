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

# _DXVACompBufferInfo structure


## -description


Specifies the requirements for compressed surfaces for DirectX Video Acceleration (DXVA).

To get this information, call <a href="https://msdn.microsoft.com/5a9fb077-fd79-4faa-a0f8-b3ac987adf36">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo</a>. Each <b>DXVACompBufferInfo</b> structure gives the requirements for a specific  DXVA surface type. The surface type is defined implicitly by the index of the array that is passed into the <i>pBufferInfo</i>  parameter.


## -struct-fields




### -field NumCompBuffers

The number of surfaces of this type to create.


### -field WidthToCreate

The width of the surface, in pixels.


### -field HeightToCreate

The height of the surface, in pixels.


### -field BytesToAllocate

The size of the surface, in bytes.


### -field Usage

A bitwise <b>OR</b> of one or more <b>D3DUSAGE</b> constants.


### -field Pool

The memory pool in which to create the surface, specified as a <b>D3DPOOL</b> value.


### -field Format

The pixel format, specified as a <b>D3DFORMAT</b> value.


## -remarks



To create the compressed surfaces, call <a href="https://msdn.microsoft.com/2bb8c99d-1151-4f6d-869f-2c1a592e76af">IDirect3DVideoDevice9::CreateSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/5a9fb077-fd79-4faa-a0f8-b3ac987adf36">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo</a>
 

 

