---
UID: NS:d3d9types._D3DDEVINFO_D3D9PIPELINETIMINGS
title: "_D3DDEVINFO_D3D9PIPELINETIMINGS"
author: windows-driver-content
description: Percent of time processing data in the pipeline.
old-location: direct3d9\d3ddevinfo_d3d9pipelinetimings.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevinfo_d3d9pipelinetimings.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 6f449248-7073-31ae-dd1f-b792e2d0e848, D3DDEVINFO_D3D9PIPELINETIMINGS, D3DDEVINFO_D3D9PIPELINETIMINGS structure [Direct3D 9], LPD3DDEVINFO_D3D9PIPELINETIMINGS, LPD3DDEVINFO_D3D9PIPELINETIMINGS structure pointer [Direct3D 9], _D3DDEVINFO_D3D9PIPELINETIMINGS, d3d9types/D3DDEVINFO_D3D9PIPELINETIMINGS, d3d9types/LPD3DDEVINFO_D3D9PIPELINETIMINGS, direct3d9.d3ddevinfo_d3d9pipelinetimings
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
req.typenames: D3DDEVINFO_D3D9PIPELINETIMINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVINFO_D3D9PIPELINETIMINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVINFO_D3D9PIPELINETIMINGS structure


## -description


Percent of time processing data in the pipeline.


## -struct-fields




### -field VertexProcessingTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percent of time spent running vertex shaders.


### -field PixelProcessingTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percent of time spent running pixel shaders.


### -field OtherGPUProcessingTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percent of time spent doing other processing.


### -field GPUIdleTimePercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Percent of time not processing anything.


## -remarks



For best performance, a balanced load is recommended.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
 

 

