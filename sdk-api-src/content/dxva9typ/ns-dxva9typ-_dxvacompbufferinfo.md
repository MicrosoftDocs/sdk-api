---
UID: NS:dxva9typ._DXVACompBufferInfo
title: "_DXVACompBufferInfo"
author: windows-sdk-content
description: Specifies the requirements for compressed surfaces for DirectX Video Acceleration (DXVA).
old-location: mf\dxvacompbufferinfo.htm
tech.root: medfound
ms.assetid: dabef388-d883-48a6-9abc-218dc163ef63
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: DXVACompBufferInfo, DXVACompBufferInfo structure [Media Foundation], _DXVACompBufferInfo, dxva9typ/DXVACompBufferInfo, mf.dxvacompbufferinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - dxva9typ.h
api_name:
 - DXVACompBufferInfo
product: Windows
targetos: Windows
req.typenames: DXVACompBufferInfo
req.redist: 
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
 

 

