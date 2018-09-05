---
UID: NS:d3d11.D3D11_TEX2DMS_ARRAY_SRV
title: D3D11_TEX2DMS_ARRAY_SRV
author: windows-sdk-content
description: Specifies the subresources from an array of multisampled 2D textures to use in a shader-resource view.
old-location: direct3d11\d3d11_tex2dms_array_srv.htm
old-project: direct3d11
ms.assetid: ce020ea2-4b2e-4d80-8ad2-5982cc7ee051
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 4eeb5c82-a7a5-65c2-774b-c2c491076826, D3D11_TEX2DMS_ARRAY_SRV, D3D11_TEX2DMS_ARRAY_SRV structure [Direct3D 11], d3d11/D3D11_TEX2DMS_ARRAY_SRV, direct3d11.d3d11_tex2dms_array_srv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_TEX2DMS_ARRAY_SRV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX2DMS_ARRAY_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEX2DMS_ARRAY_SRV structure


## -description


Specifies the subresources from an array of multisampled 2D textures to use in a shader-resource view.


## -struct-fields




### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures.


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

