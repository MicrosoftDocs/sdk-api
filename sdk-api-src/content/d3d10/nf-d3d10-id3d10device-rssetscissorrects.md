---
UID: NF:d3d10.ID3D10Device.RSSetScissorRects
title: ID3D10Device::RSSetScissorRects
author: windows-sdk-content
description: Bind an array of scissor rectangles to the rasterizer stage.
old-location: direct3d10\id3d10device_rssetscissorrects.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetscissorrects.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSSetScissorRects method, ID3D10Device.RSSetScissorRects, ID3D10Device::RSSetScissorRects, RSSetScissorRects, RSSetScissorRects method [Direct3D 10], RSSetScissorRects method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSSetScissorRects, direct3d10.id3d10device_rssetscissorrects, ff11533a-fe9e-059e-c169-7e6f3c873b2d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Device.RSSetScissorRects
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::RSSetScissorRects


## -description


Bind an array of <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">scissor rectangles</a> to the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a>.


## -parameters




### -param NumRects [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of scissor rectangles to bind.


### -param pRects [in]

Type: <b>const <a href="https://msdn.microsoft.com/a0b27fb0-1e48-4e46-ad8c-99f197c31dc2">D3D10_RECT</a>*</b>

An array of scissor rectangles (see <a href="https://msdn.microsoft.com/a0b27fb0-1e48-4e46-ad8c-99f197c31dc2">D3D10_RECT</a>).


## -returns



Returns nothing.




## -remarks



The scissor rectangles will only be used if ScissorEnable is set to true in the rasterizer state (see <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">D3D10_RASTERIZER_DESC</a>).

Which scissor rectangle to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">shader semantic syntax</a>). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first scissor rectangle in the array.

Each scissor rectangle in the array corresponds to a viewport in an array of viewports (see <a href="https://msdn.microsoft.com/d622c531-8cd5-46f6-82dd-27a202c2b58f">ID3D10Device::RSSetViewports</a>).




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

