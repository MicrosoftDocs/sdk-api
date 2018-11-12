---
UID: NS:d3d11.D3D11_TEX2D_ARRAY_VPOV
title: D3D11_TEX2D_ARRAY_VPOV
author: windows-sdk-content
description: Identifies a texture resource for a video processor output view.
old-location: mf\d3d11_tex2d_array_vpov.htm
tech.root: medfound
ms.assetid: DF059392-3E4B-45D2-A3CD-A0C61C8D628F
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D11_TEX2D_ARRAY_VPOV, D3D11_TEX2D_ARRAY_VPOV structure [Media Foundation], d3d11/D3D11_TEX2D_ARRAY_VPOV, mf.d3d11_tex2d_array_vpov
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - D3D11_TEX2D_ARRAY_VPOV
product: Windows
targetos: Windows
req.typenames: D3D11_TEX2D_ARRAY_VPOV
req.redist: 
---

# D3D11_TEX2D_ARRAY_VPOV structure


## -description


Identifies a texture resource for a video  processor output view.


## -struct-fields




### -field MipSlice

The zero-based index into the array of subtextures.


### -field FirstArraySlice

The index of the first texture to use.


### -field ArraySize

The number of textures in the array.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/EC7AFE44-877C-4FB0-9E61-FCD504A334D3">ID3D11VideoDevice::CreateVideoProcessorOutputView</a>
 

 

