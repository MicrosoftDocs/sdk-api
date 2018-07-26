---
UID: NS:d3d11.D3D11_TEX2DMS_ARRAY_RTV
title: D3D11_TEX2DMS_ARRAY_RTV
author: windows-sdk-content
description: Specifies the subresources from a an array of multisampled 2D textures to use in a render-target view.
old-location: direct3d11\d3d11_tex2dms_array_rtv.htm
old-project: direct3d11
ms.assetid: ec08341c-980f-4d5f-8eb9-f41835105b46
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D11_TEX2DMS_ARRAY_RTV, D3D11_TEX2DMS_ARRAY_RTV structure [Direct3D 11], d3d11/D3D11_TEX2DMS_ARRAY_RTV, dd9c5839-fcab-1f5f-a4fe-866cc00f6bd2, direct3d11.d3d11_tex2dms_array_rtv
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
tech.root: 
req.typenames: D3D11_TEX2DMS_ARRAY_RTV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX2DMS_ARRAY_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEX2DMS_ARRAY_RTV structure


## -description


Specifies the subresources from a an array of multisampled 2D textures to use in a render-target view.


## -struct-fields




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
 

 

