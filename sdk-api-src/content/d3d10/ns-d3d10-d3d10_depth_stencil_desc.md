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

# D3D10_DEPTH_STENCIL_DESC structure


## -description


Describes depth-stencil state.


## -struct-fields




### -field DepthEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that enables depth testing.  The default value is <b>TRUE</b>.


### -field DepthWriteMask

Type: <b><a href="https://msdn.microsoft.com/16bca9bc-a75d-49e7-9032-1930623018f2">D3D10_DEPTH_WRITE_MASK</a></b>

A member of the <a href="https://msdn.microsoft.com/16bca9bc-a75d-49e7-9032-1930623018f2">D3D10_DEPTH_WRITE_MASK</a> enumerated type that identifies a portion of the depth-stencil buffer that can be modified by depth data.  The default value is <b>D3D10_DEPTH_WRITE_MASK_ALL</b>.


### -field DepthFunc

Type: <b><a href="https://msdn.microsoft.com/e0d0d421-ebd0-441c-949b-97506703e3fa">D3D10_COMPARISON_FUNC</a></b>

A member of the <a href="https://msdn.microsoft.com/e0d0d421-ebd0-441c-949b-97506703e3fa">D3D10_COMPARISON_FUNC</a> enumerated type that defines how depth data is compared against existing depth data.  The default value is <b>D3D10_COMPARISON_LESS</b>


### -field StencilEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that enables stencil testing.  The default value is <b>FALSE</b>.


### -field StencilReadMask

Type: <b>UINT8</b>

A value that identifies a portion of the depth-stencil buffer for reading stencil data.  The default value is <b>D3D10_DEFAULT_STENCIL_READ_MASK</b>.


### -field StencilWriteMask

Type: <b>UINT8</b>

A value that identifies a portion of the depth-stencil buffer for writing stencil data. The default value is <b>D3D10_DEFAULT_STENCIL_WRITE_MASK</b>.


### -field FrontFace

Type: <b><a href="https://msdn.microsoft.com/d7fac8af-cd84-4aae-9e62-d5394e79f53c">D3D10_DEPTH_STENCILOP_DESC</a></b>

A <a href="https://msdn.microsoft.com/d7fac8af-cd84-4aae-9e62-d5394e79f53c">D3D10_DEPTH_STENCILOP_DESC</a> structure that identifies how to use the results of the depth test and the stencil test for pixels whose surface normal is facing toward the camera.


### -field BackFace

Type: <b><a href="https://msdn.microsoft.com/d7fac8af-cd84-4aae-9e62-d5394e79f53c">D3D10_DEPTH_STENCILOP_DESC</a></b>

A <a href="https://msdn.microsoft.com/d7fac8af-cd84-4aae-9e62-d5394e79f53c">D3D10_DEPTH_STENCILOP_DESC</a> structure that identifies how to use the results of the depth test and the stencil test for pixels whose surface normal is facing away from the camera.


## -remarks



Depth-stencil state controls how <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> testing is performed by the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger</a> stage.

The formats that support stenciling are DXGI_FORMAT_D24_UNORM_S8_UINT and DXGI_FORMAT_D32_FLOAT_S8X24_UINT.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

