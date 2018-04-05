---
UID: NS:d3d9types._D3DDEVINFO_D3D9BANDWIDTHTIMINGS
title: "_D3DDEVINFO_D3D9BANDWIDTHTIMINGS"
author: windows-driver-content
description: Throughput metrics for help in understanding the performance of an application.
old-location: direct3d9\d3ddevinfo_d3d9bandwidthtimings.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevinfo_d3d9bandwidthtimings.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DDEVINFO_D3D9BANDWIDTHTIMINGS, D3DDEVINFO_D3D9BANDWIDTHTIMINGS structure [Direct3D 9], LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS, LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS structure pointer [Direct3D 9], _D3DDEVINFO_D3D9BANDWIDTHTIMINGS, c43cf83c-fe17-514d-7bfe-9747219c4a4f, d3d9types/D3DDEVINFO_D3D9BANDWIDTHTIMINGS, d3d9types/LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS, direct3d9.d3ddevinfo_d3d9bandwidthtimings
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
req.typenames: D3DDEVINFO_D3D9BANDWIDTHTIMINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVINFO_D3D9BANDWIDTHTIMINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVINFO_D3D9BANDWIDTHTIMINGS structure


## -description


Throughput metrics for help in understanding the performance of an application.


## -struct-fields




### -field MaxBandwidthUtilized

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

The bandwidth or maximum data transfer rate from the host CPU to the GPU. This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.


### -field FrontEndUploadMemoryUtilizedPercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Memory utilized percentage when uploading data from the host CPU to the GPU. 


### -field VertexRateUtilizedPercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Vertex throughput percentage. This is the number of vertices processed compared to the theoretical maximum vertex processing rate.


### -field TriangleSetupRateUtilizedPercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Triangle set-up throughput percentage. This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.


### -field FillRateUtilizedPercent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Pixel fill throughput percentage. This is the number of pixels that are filled compared to the theoretical pixel fill.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
 

 

