---
UID: NS:d3d12.D3D12_TEX3D_RTV
title: D3D12_TEX3D_RTV
author: windows-driver-content
description: Describes the subresources from a 3D texture to use in a render-target view.
old-location: direct3d12\d3d12_tex3d_rtv.htm
old-project: direct3d12
ms.assetid: D640C247-FDE9-49DD-88AB-BCCC3B8880D1
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: D3D12_TEX3D_RTV, D3D12_TEX3D_RTV structure, d3d12/D3D12_TEX3D_RTV, direct3d12.d3d12_tex3d_rtv
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D12_TEX3D_RTV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_TEX3D_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_TEX3D_RTV structure


## -description


Describes the subresources from a 3D texture to use in a render-target view.


## -struct-fields




### -field MipSlice

The index of the mipmap level to use mip slice.


### -field FirstWSlice

First depth level to use.


### -field WSize

Number of depth levels to use in the render-target view, starting from <b>FirstWSlice</b>. A value of -1 indicates all of the slices along the w axis, starting from <b>FirstWSlice</b>.


## -remarks



Use this structure with a <a href="https://msdn.microsoft.com/D8602EB9-70EB-4A4E-8D8D-A2016335AAC6">D3D12_RENDER_TARGET_VIEW_DESC</a> structure to view the resource as a 3D texture.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

