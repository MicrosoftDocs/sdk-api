---
UID: NS:d3d11.D3D11_TEX1D_ARRAY_RTV
title: D3D11_TEX1D_ARRAY_RTV
author: windows-sdk-content
description: Specifies the subresources from an array of 1D textures to use in a render-target view.
old-location: direct3d11\d3d11_tex1d_array_rtv.htm
tech.root: direct3d11
ms.assetid: cdb1c9e0-39a4-415e-a91f-05042b1f1b2d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 9b2f38aa-7062-6fcf-c263-f4aa1f05a173, D3D11_TEX1D_ARRAY_RTV, D3D11_TEX1D_ARRAY_RTV structure [Direct3D 11], d3d11/D3D11_TEX1D_ARRAY_RTV, direct3d11.d3d11_tex1d_array_rtv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
 - D3D11.h
api_name:
 - D3D11_TEX1D_ARRAY_RTV
product: Windows
targetos: Windows
req.typenames: D3D11_TEX1D_ARRAY_RTV
req.redist: 
---

# D3D11_TEX1D_ARRAY_RTV structure


## -description


Specifies the subresources from an array of 1D textures to use in a render-target view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the mipmap level to use mip slice.


### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures.


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a render-target-view description (see <a href="https://msdn.microsoft.com/b154ac98-49ed-4d00-8cb6-5e57680e125c">D3D11_RENDER_TARGET_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

