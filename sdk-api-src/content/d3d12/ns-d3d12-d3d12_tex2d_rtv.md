---
UID: NS:d3d12.D3D12_TEX2D_RTV
title: D3D12_TEX2D_RTV
author: windows-sdk-content
description: Describes the subresource from a 2D texture to use in a render-target view.
old-location: direct3d12\d3d12_tex2d_rtv.htm
tech.root: direct3d12
ms.assetid: E85CC5DF-96A9-488E-95A3-60175FA7B63E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: D3D12_TEX2D_RTV, D3D12_TEX2D_RTV structure, d3d12/D3D12_TEX2D_RTV, direct3d12.d3d12_tex2d_rtv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
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
 - D3D12.h
api_name:
 - D3D12_TEX2D_RTV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX2D_RTV
req.redist: 
---

# D3D12_TEX2D_RTV structure


## -description


Describes the subresource from a 2D texture to use in a render-target view.


## -struct-fields




### -field MipSlice

The index of the mipmap level to use.


### -field PlaneSlice

The index (plane slice number) of the plane to use in the texture.
          


## -remarks



Use this structure with a <a href="https://msdn.microsoft.com/D8602EB9-70EB-4A4E-8D8D-A2016335AAC6">D3D12_RENDER_TARGET_VIEW_DESC</a> structure to view the resource as a 2D texture.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

