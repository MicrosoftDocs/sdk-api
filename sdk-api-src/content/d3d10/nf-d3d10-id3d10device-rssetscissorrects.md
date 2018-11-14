---
UID: NF:d3d10.ID3D10Device.RSSetScissorRects
title: ID3D10Device::RSSetScissorRects
author: windows-sdk-content
description: Bind an array of scissor rectangles to the rasterizer stage.
old-location: direct3d10\id3d10device_rssetscissorrects.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetscissorrects.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSSetScissorRects method, ID3D10Device.RSSetScissorRects, ID3D10Device::RSSetScissorRects, RSSetScissorRects, RSSetScissorRects method [Direct3D 10], RSSetScissorRects method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSSetScissorRects, direct3d10.id3d10device_rssetscissorrects, ff11533a-fe9e-059e-c169-7e6f3c873b2d
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.RSSetScissorRects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.RSSetScissorRects
: 
---

# ID3D10Device::RSSetScissorRects


## -description


Bind an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">scissor rectangles</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>.


## -parameters




### -param NumRects [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of scissor rectangles to bind.


### -param pRects [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb232915(v=VS.85).aspx">D3D10_RECT</a>*</b>

An array of scissor rectangles (see <a href="https://msdn.microsoft.com/en-us/library/Bb232915(v=VS.85).aspx">D3D10_RECT</a>).


## -returns



Returns nothing.




## -remarks



The scissor rectangles will only be used if ScissorEnable is set to true in the rasterizer state (see <a href="https://msdn.microsoft.com/en-us/library/Bb172408(v=VS.85).aspx">D3D10_RASTERIZER_DESC</a>).

Which scissor rectangle to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see <a href="https://msdn.microsoft.com/en-us/library/Bb509647(v=VS.85).aspx">shader semantic syntax</a>). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first scissor rectangle in the array.

Each scissor rectangle in the array corresponds to a viewport in an array of viewports (see <a href="https://msdn.microsoft.com/en-us/library/Bb173613(v=VS.85).aspx">ID3D10Device::RSSetViewports</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

