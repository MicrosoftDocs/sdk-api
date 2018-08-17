---
UID: NS:d3d10.D3D10_TEX2D_ARRAY_DSV
title: D3D10_TEX2D_ARRAY_DSV
author: windows-sdk-content
description: Specifies the subresource(s) from an array 2D textures that are accessible to a depth-stencil view.
old-location: direct3d10\d3d10_tex2d_array_dsv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2d_array_dsv.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: D3D10_TEX2D_ARRAY_DSV, D3D10_TEX2D_ARRAY_DSV structure [Direct3D 10], b74f90e0-46e3-78ef-850f-dc574308fe4b, d3d10/D3D10_TEX2D_ARRAY_DSV, direct3d10.d3d10_tex2d_array_dsv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_TEX2D_ARRAY_DSV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEX2D_ARRAY_DSV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEX2D_ARRAY_DSV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource(s)</a> from an array <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D textures</a> that are accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first mipmap level to use (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">mip slice</a>).


### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">array slice</a>)


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a depth-stencil-view description (see <a href="https://msdn.microsoft.com/7e427a75-99d7-4a18-afee-077bee01683c">D3D10_DEPTH_STENCIL_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

