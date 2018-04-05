---
UID: NS:d3d9types._D3DDEVINFO_D3D9CACHEUTILIZATION
title: "_D3DDEVINFO_D3D9CACHEUTILIZATION"
author: windows-driver-content
description: Measure the cache hit rate performance for textures and indexed vertices.
old-location: direct3d9\d3ddevinfo_d3d9cacheutilization.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevinfo_d3d9cacheutilization.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 753a7bac-750c-16de-f157-3395bf81ff80, D3DDEVINFO_D3D9CACHEUTILIZATION, D3DDEVINFO_D3D9CACHEUTILIZATION structure [Direct3D 9], LPD3DDEVINFO_D3D9CACHEUTILIZATION, LPD3DDEVINFO_D3D9CACHEUTILIZATION structure pointer [Direct3D 9], _D3DDEVINFO_D3D9CACHEUTILIZATION, d3d9types/D3DDEVINFO_D3D9CACHEUTILIZATION, d3d9types/LPD3DDEVINFO_D3D9CACHEUTILIZATION, direct3d9.d3ddevinfo_d3d9cacheutilization
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DDEVINFO_D3D9CACHEUTILIZATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVINFO_D3D9CACHEUTILIZATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVINFO_D3D9CACHEUTILIZATION structure


## -description


Measure the cache hit rate performance for textures and indexed vertices.


## -struct-fields




### -field TextureCacheHitRate

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

The hit rate for finding a texture in the texture cache. This assumes there is a texture cache. Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.


### -field PostTransformVertexCacheHitRate

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

The hit rate for finding transformed vertices in the vertex cache. The GPU is designed to transform indexed vertices and may store them in a vertex cache. If you are using meshes, <a href="https://msdn.microsoft.com/428c2af8-43e7-4cf7-8b9b-04ba5cff82c8">D3DXOptimizeFaces</a> or <a href="https://msdn.microsoft.com/a3b9cb68-204e-4e8f-a985-738d1cea1e29">D3DXOptimizeVertices</a> may result in better vertex cache utilization.


## -remarks



An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
 

 

