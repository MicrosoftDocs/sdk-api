---
UID: NS:d3d10.D3D10_DEPTH_STENCIL_DESC
title: D3D10_DEPTH_STENCIL_DESC
author: windows-sdk-content
description: Describes depth-stencil state.
old-location: direct3d10\d3d10_depth_stencil_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_depth_stencil_desc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_DEPTH_STENCIL_DESC, D3D10_DEPTH_STENCIL_DESC structure [Direct3D 10], bc44a5f2-b12b-88c0-0985-df3e7b45b998, d3d10/D3D10_DEPTH_STENCIL_DESC, direct3d10.d3d10_depth_stencil_desc
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
 - D3D10_DEPTH_STENCIL_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_DEPTH_STENCIL_DESC
req.redist: 
---

# D3D10_DEPTH_STENCIL_DESC structure


## -description


Describes depth-stencil state.


## -struct-fields




### -field DepthEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that enables depth testing.  The default value is <b>TRUE</b>.


### -field DepthWriteMask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205038(v=VS.85).aspx">D3D10_DEPTH_WRITE_MASK</a></b>

A member of the <a href="https://msdn.microsoft.com/en-us/library/Bb205038(v=VS.85).aspx">D3D10_DEPTH_WRITE_MASK</a> enumerated type that identifies a portion of the depth-stencil buffer that can be modified by depth data.  The default value is <b>D3D10_DEPTH_WRITE_MASK_ALL</b>.


### -field DepthFunc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204902(v=VS.85).aspx">D3D10_COMPARISON_FUNC</a></b>

A member of the <a href="https://msdn.microsoft.com/en-us/library/Bb204902(v=VS.85).aspx">D3D10_COMPARISON_FUNC</a> enumerated type that defines how depth data is compared against existing depth data.  The default value is <b>D3D10_COMPARISON_LESS</b>


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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205035(v=VS.85).aspx">D3D10_DEPTH_STENCILOP_DESC</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb205035(v=VS.85).aspx">D3D10_DEPTH_STENCILOP_DESC</a> structure that identifies how to use the results of the depth test and the stencil test for pixels whose surface normal is facing toward the camera.


### -field BackFace

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205035(v=VS.85).aspx">D3D10_DEPTH_STENCILOP_DESC</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb205035(v=VS.85).aspx">D3D10_DEPTH_STENCILOP_DESC</a> structure that identifies how to use the results of the depth test and the stencil test for pixels whose surface normal is facing away from the camera.


## -remarks



Depth-stencil state controls how <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">depth-stencil</a> testing is performed by the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger</a> stage.

The formats that support stenciling are DXGI_FORMAT_D24_UNORM_S8_UINT and DXGI_FORMAT_D32_FLOAT_S8X24_UINT.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205153(v=VS.85).aspx">Core Structures</a>
 

 

