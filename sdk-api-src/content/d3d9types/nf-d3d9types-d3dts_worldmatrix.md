---
UID: NF:d3d9types.D3DTS_WORLDMATRIX
title: D3DTS_WORLDMATRIX macro
author: windows-driver-content
description: Maps indices in the range 0 through 255 to the corresponding transform states.
old-location: direct3d9\d3dts_worldmatrix.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dts_worldmatrix.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 6860afd7-7a6e-bb9d-f8d1-8862d14133c4, D3DTS_WORLDMATRIX, D3DTS_WORLDMATRIX macro [Direct3D 9], d3d9types/D3DTS_WORLDMATRIX, direct3d9.d3dts_worldmatrix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: D3DZBUFFERTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3d9types.h
api_name:
-	D3DTS_WORLDMATRIX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DTS_WORLDMATRIX macro


## -description


Maps indices in the range 0 through 255 to the corresponding transform states.


## -parameters




### -param index

An index value in the range 0 through 255.


## -remarks



Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.




## -see-also




<a href="https://msdn.microsoft.com/cabb715a-2a6a-4d56-8113-5e5ed26fc107">Macros</a>



<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">SetTransform</a>
 

 

