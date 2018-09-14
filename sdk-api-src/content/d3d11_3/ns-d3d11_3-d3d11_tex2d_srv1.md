---
UID: NS:d3d11_3.D3D11_TEX2D_SRV1
title: D3D11_TEX2D_SRV1
author: windows-sdk-content
description: Describes the subresource from a 2D texture to use in a shader-resource view.
old-location: direct3d11\d3d11_tex2d_srv1.htm
tech.root: direct3d11
ms.assetid: 5C5D8BF8-1B3E-4FEF-ACD7-FCEAEE335DFE
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: D3D11_TEX2D_SRV1, D3D11_TEX2D_SRV1 structure [Direct3D 11], d3d11_3/D3D11_TEX2D_SRV1, direct3d11.d3d11_tex2d_srv1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_3.h
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
 - D3D11_3.h
api_name:
 - D3D11_TEX2D_SRV1
product: Windows
targetos: Windows
req.typenames: D3D11_TEX2D_SRV1
req.redist: 
---

# D3D11_TEX2D_SRV1 structure


## -description


Describes the subresource from a 2D texture to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Index of the most detailed mipmap level to use; this number is between 0 and (<b>MipLevels</b> (from the original Texture2D for which 
            <a href="https://msdn.microsoft.com/50E072F2-EC3E-4BED-A230-5447ECD1E7D6">ID3D11Device3::CreateShaderResourceView1</a>creates a view) - 1 ).
          


### -field MipLevels

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a>.
            

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.
            


### -field PlaneSlice

The index (plane slice number) of the plane to use in the texture.


## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

